  # Common questions
  
  ---
  
  ## Getting oriented
  
  **What is Glade?**
  
  Glade is a privacy-first crypto neobank on Robinhood Chain, which is Robinhood's AI-native Ethereum Layer 2. It gives you a self-custodied account for USDG and ETH. Transfer amounts are encrypted by default, payments settle in the next block (roughly 100ms), and people and AI agents hold accounts side by side.
  
  **Do I need to understand blockchains to use it?**
  
  No. You sign up with an email address and a passkey, which feels much like enabling Face ID in any other app. Key management, encryption and settlement all run in the background without you having to handle them.
  
  **What currencies does it support?**
  
  It holds USDG, the Global Dollar that Paxos issues natively on Robinhood Chain, and it also accepts bridged USDC. Glade keeps a small ETH balance topped up for you to cover gas, so network fees are never something you have to plan for.
  
  **Will I be anonymous?**
  
  You won't, and that's by design. We verify your identity when you open an account, and your address can be seen on-chain. What stays private is the amount of money moving through the account. That is confidentiality, which is different from anonymity, and [Regulation](../trust/regulation.md) explains why the distinction matters.
  
  ---
  
  ## Personal accounts
  
  **How are my amounts kept private?**
  
  Your transfers run through confidential token contracts. These are ERC-20 tokens with encrypted balances, where every amount is stored as an ElGamal ciphertext. Your device produces zero-knowledge proofs, and a verifier on-chain checks them. The only people who can decrypt an amount are you and your counterparty. [Hidden amounts](../confidentiality/hidden-amounts.md) has the full explanation.
  
  **Can anyone see my balance?**
  
  They can't. Your on-chain balance is a ciphertext, and only your key decrypts it. Someone watching the chain can see that your address exists and holds a balance, but they can't tell how much is in it.
  
  **A landlord or an auditor wants proof that I paid. What should I do?**
  
  Generate a disclosure proof covering just that one payment. You choose what it reveals and who receives it, and it reveals nothing beyond that. [Payment receipts](../confidentiality/payment-receipts.md) shows how.
  
  **My phone is gone. How do I get back in?**
  
  When your passkey is synced through iCloud Keychain or Google Password Manager, signing in on a different device restores access right away. You can also use a key you exported beforehand. Details are in [Keys and restoring access](../confidentiality/keys-and-restoring-access.md).
  
  **Does Glade store my transaction history in readable form anywhere?**
  
  No. Your device uses your key to decrypt and display your history. Glade's servers only ever handle ciphertext and public metadata, so they hold nothing readable that could leak.
  
  ---
  
  ## Agents
  
  **So what exactly is an agent account?**
  
  An agent receives its own wallet on Robinhood Chain along with an Agent ID that is nested under a parent account. It spends according to a policy that the parent controls, covering daily limits, approved recipients and hours, with an optional threshold above which a payment needs approval. Start with [Agent accounts](../agents/agent-accounts.md).
  
  **Is it possible for an agent to go over the limits I set?**
  
  No. The policy is enforced before a transaction is signed, rather than checked after the fact. A payment that would break the rules never gets built, so there's never anything to reverse. [Spending rules](../agents/spending-rules.md) covers the details.
  
  **Can agents pay with x402?**
  
  They can. x402 support is built into every agent account. See [Pay per request](../agents/pay-per-request.md).
  
  **How can I find out when one of my agents makes a payment?**
  
  Subscribe to webhook events. Instructions are on the [Live events](../agents/live-events.md) page and in the [Webhooks API](../reference/webhooks-api.md) reference.
  
  **Will the API return an agent's amounts?**
  
  Not in readable form. You'd need to decrypt them on your side with your own key. The API never sends plaintext amounts, because Glade's servers don't have a decryption key either, and that holds at every step.
  
  ---
  
  ## Compliance
  
  **If Glade is about privacy, why is KYC required?**
  
  Confidential amounts and anonymity are two separate things. Glade hides amounts, not identities. Every account is tied to a verified person or entity, and that is exactly what allows Glade to work within the GENIUS Act framework and to answer lawful process when it's required to.
  
  **What happens with large or cross-border payments?**
  
  When a payment goes over the regulatory thresholds, Travel Rule requirements apply to it, and that includes screening the counterparty. [Identity checks](../trust/identity-checks.md) goes into more detail.
  
  **Is Glade open source?**
  
  The confidential transfer layer is. That means the token contracts and the on-chain verifier, which anyone can audit on Robinhood Chain. The application layer, made up of the app, the backend and the indexer, stays closed source for the duration of the beta.
  
  ---
  
  ## Fees
  
  **What does it cost to send a transfer?**
  
  Glade takes no fee during the beta. You pay only Robinhood Chain gas, which is typically a fraction of a cent and comes out of your ETH float automatically.
  
  **Do I pay to use the API?**
  
  Not during the beta. After the beta, the revenue model is expected to add a metered tier for agents that generate high volumes of traffic.
  
