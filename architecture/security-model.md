  # Security model
  
  You should not have to trust Glade, the company, for your money to stay yours, for transfers to be valid, or for amounts to stay private. The system is layered so that each of those properties rests on its own mechanism, and each one is meant to survive a scenario where Glade itself is acting against you.
  
  ---
  
  ## Each layer, its threat and its defense
  
  | Layer | What could go wrong | How it is handled |
  |---|---|---|
  | Custody | Glade gets hacked, or someone pressures it to move funds | Keys are created and kept on your device, and the system is non-custodial. No private key is ever in Glade's hands. |
  | Confidentiality | Glade or an outside party attempts to read amounts | The client does the proving and the decrypting. Glade's backend sees nothing but ciphertext. |
  | Transfer validity | A transfer is malformed or would push a balance below zero | The on-chain verifier checks range and validity proofs before touching any balance. Robinhood Chain settles to Ethereum through fraud proofs on the Arbitrum stack, so Ethereum ultimately secures that check. |
  | Agent overspend | An agent attempts a payment its owner did not allow | `AgentController` stores each policy on-chain and refuses any spend that violates it. The client runs the same checks first, before anything is signed. |
  | Key loss | You lose your device and your passkey together | Passkeys sync between devices, keys can be exported, and social recovery is planned for after the beta. Details are in [Keys and restoring access](../confidentiality/keys-and-restoring-access.md). |
  | Replay or forgery | Someone reuses or fakes a signed transaction | Standard EVM signatures and account nonces apply, the same as for every Robinhood Chain transaction. |
  | Censorship | The sequencer stops, or refuses to include a transaction | Robinhood runs one sequencer at present. If it skips a transaction, the Arbitrum stack's delayed inbox on Ethereum guarantees it still gets included. |
  | Availability | Glade's backend goes down | Your funds sit in smart accounts you own on Robinhood Chain, not in contracts under Glade's control. Export your key and any EVM wallet can reach them. |
  
  ---
  
  ## Glade's powers and their limits
  
  Glade does have a role. It can:
  
  - Serve the app, route requests, and turn chain events into a live feed
  - Set up webhooks and deliver them
  - Run a spend policy check when an agent's client is about to sign
  - Handle the KYC and disclosure flows, when you are the one who starts them
  
  Glade is unable to:
  
  - Move funds without your signature. It holds none of your private keys.
  - Read your amounts. It holds none of your decryption keys.
  - Change a transaction you have signed. A bad signature is rejected by the chain, and a missing or invalid proof is rejected by the verifier.
  - Overrule an agent's policy. `AgentController` enforces the limits on-chain and the client checks them before signing. No backend gets to decide case by case.
  
  The second list matters more. Every entry on it is guaranteed by cryptography and consensus, rather than by a commitment written into a policy.
  
  ---
  
  ## Proofs are generated on your device
  
  The zero-knowledge proofs behind confidential transfers are produced in WASM on your own device. Glade's servers never generate them. This is a property of how the system is built, not a rule Glade chose to follow: plaintext balances and amounts are never present anywhere Glade's infrastructure could record them, regardless of intent. The sequencer orders ciphertext and never encounters a balance or an amount.
  
  ---
  
  ## Why Glade runs its own RPC
  
  Glade operates RPC infrastructure of its own so the app holds up under heavy traffic, rather than leaning on public Robinhood Chain endpoints. The reason is performance. Trust does not come into it.
  
  Each transaction Glade sends is a normal signed Robinhood Chain transaction, which any other provider could submit equally well. If every provider failed, it could still be forced onto the chain through Ethereum's delayed inbox. No route is privileged, and nobody sits at the gate.
  
  ---
  
  ## Retrying without double-spending
  
  Each submission is bound to a specific account nonce. If a shaky connection causes a transaction to be resent, the chain will still include it only once. Since submission is idempotent and relies on ordinary EVM nonces, an accidental duplicate send is not possible.
  
  ---
  
  ## Risks that remain, and how they are reduced
  
  | Risk | How it is reduced |
  |---|---|
  | You lose a device and had no synced passkey | Export your key in advance and store it safely. Social recovery is coming after the beta. |
  | Your device cannot generate proofs fast enough | Proving can be assisted by the server, using inputs the client derives. Plaintext amounts are never sent. |
  | Someone compromises the parent account | Policy limits bound the loss even when a session is hijacked. Revoke the agent's key in the dashboard straight away. |
  | Regulators move against the company | Funds stay in smart accounts that users own, not in accounts Glade has custody of. Access on-chain keeps working whatever happens to the company. |
  | The sequencer or network fails | There are several RPC providers and a status page, and forced inclusion through Ethereum's delayed inbox remains an option. Service might slow down, but funds are not at risk. |
  
