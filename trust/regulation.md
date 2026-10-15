  # Regulation
  
  Glade's approach to compliance rests on a single distinction: amounts are confidential, but people are not anonymous. Your address is visible to anyone, and so is the fact that a verified identity stands behind it. What stays hidden is the amounts, unless you reveal one yourself or lawful process requires it. Everything below follows from that.
  
  ---
  
  ## Which laws apply
  
  Glade operates under the GENIUS Act, the US law for regulated stablecoins passed in July 2025. USDG, Paxos' Global Dollar, is issued natively on Robinhood Chain and satisfies that framework. Bridged USDC, which Glade also accepts, satisfies it as well. Glade's stablecoin operations are structured to align with the Act.
  
  ---
  
  ## Every account is verified
  
  Verification happens when an account is opened, with no exceptions. Personal accounts, Business accounts and the parent account that sits behind every Agent all go through it. You can verify at one of two levels.
  
  | Level | What you provide | What you get |
  |---|---|---|
  | Basic | A government ID and a liveness check | Standard limits |
  | Enhanced | Further documents and proof of address | Higher limits, plus Business features |
  
  Anonymous and pseudonymous accounts aren't available. The money moving through an account is encrypted, but the account itself always belongs to a verified person or entity.
  
  See [Identity checks](identity-checks.md) for the full process and limits.
  
  ---
  
  ## The Travel Rule
  
  The Travel Rule applies to cross-border payments and to payments above the threshold. Glade meets it in these ways:
  
  - When a counterparty's compliance system needs it, Glade supplies disclosure proofs (covered in [Identity checks](identity-checks.md))
  - Counterparty addresses are screened through Chainalysis or TRM Labs
  - Where it applies, identity details pass between the regulated originating and beneficiary institutions using the standard exchange
  
  ---
  
  ## Where Glade is available
  
  The beta is open in the United States and in a selection of EU jurisdictions. It is not accessible from places that expressly prohibit crypto payment services.
  
  ---
  
  ## Where data is stored
  
  Profile data and KYC records are stored in a region matching the place each account was opened. On-chain data works differently. It is global by design, living on Robinhood Chain and settling to Ethereum rather than sitting in Glade's systems. Onboarding spells this out so you know before you start.
  
  ---
  
  ## Privacy and compliance together
  
  The confidential token layer conceals amounts. It does not conceal identities. Addresses are public and permanently tied to a verified owner. If a lawful request concerns a specific account, it can be answered through the disclosure mechanism explained in [Payment receipts](../confidentiality/payment-receipts.md).
  
  Regulated payment systems that preserve privacy have mostly converged on this model of confidentiality without anonymity. Glade built its entire contract layer around it, so the system is accountable wherever the law calls for it and confidential everywhere else.
  
  ---
  
  ## Related pages
  
  - [Identity checks](identity-checks.md)
  - [Payment receipts](../confidentiality/payment-receipts.md)
  
