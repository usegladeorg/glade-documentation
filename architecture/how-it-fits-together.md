  # How it fits together
  
  Glade provides confidential payments for people and for the software that acts for them. It runs on Robinhood Chain. Privacy comes from Glade's own confidential token contracts, an ERC-20 with encrypted balances that follows the Zether line of designs. The EVM offers nothing like this natively, so Glade wrote the contract layer itself and verified it on-chain. Glade also differs from a typical fintech in that it keeps no settlement ledger of its own. Robinhood Chain is the ledger, with Ethereum underneath it.
  
  ## What the system is responsible for
  
  | Area | How it works |
  |---|---|
  | Custody and signing | Each account is an ERC-4337 smart account controlled by a keypair generated on the client. The keys never reach Glade. |
  | Confidential transfers | Amounts are encrypted by the token contracts. Proofs are produced on the client. |
  | Gas abstraction | Every account holds a small ETH float that refills through an internal swap when it gets low. Users only deal in USDG and never have to think about gas. |
  | Agent policy | Spend policies are checked by the agent's client during signing and enforced on-chain by the `AgentController` contract. |
  | Indexing | An off-chain indexer reads contract event streams and feeds both the live activity feed and webhooks. Nothing polls. |
  
  The design rests on one split. Questions that need trust, such as who owns which funds or whether a transfer is valid, are settled by Robinhood Chain and Glade's on-chain contracts. The rollup's fraud-proof settlement then ties that correctness back to Ethereum. The rest (rendering, notifications, indexing) is convenience layered on top and is never the source of truth.
  
  ## The layers
  
  
