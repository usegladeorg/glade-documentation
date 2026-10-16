  # Identity checks
  
  This page explains how Glade confirms who owns an account and what happens with cross-border requirements when a payment goes over the applicable threshold.
  
  ---
  
  ## Getting verified
  
  Verification happens once, at account creation. It runs through Glade's verification provider, which is Persona or a similar regulated vendor.
  
  1. Take a photo of your government-issued ID and upload it.
  2. Complete a liveness check by recording a brief selfie video, which is matched against your ID photo.
  3. Wait for the result. Most people are approved within minutes, though some cases are passed to a human reviewer.
  
  ### Enhanced verification
  
  You need enhanced verification for higher limits or to open a Business account. On top of the basic steps, it asks for:
  
  - Proof of address, such as a recent utility bill or bank statement
  - Standard KYB documents for Business accounts, covering incorporation and beneficial ownership
  
  ---
  
  ## Levels and daily limits
  
  | Level | Daily limit | What's required |
  |---|---|---|
  | Basic | Up to $2,500 | Government ID and a liveness check |
  | Enhanced | Up to $25,000 | All Basic requirements, plus proof of address |
  | Business | Negotiated | KYB documents and beneficial owner disclosure |
  
  If you need more than the Business level allows, the request is assessed individually, and the compliance team is usually involved directly.
  
  ---
  
  ## How Glade handles the Travel Rule
  
  The Travel Rule requires financial institutions to pass along originator and beneficiary details for transfers above a threshold. Each jurisdiction sets its own threshold. In the United States it is $3,000.
  
  Glade's approach has three parts.
  
  **Screening.** A payment over the threshold doesn't settle until the receiving address has been checked against sanctions and risk lists, using Chainalysis or TRM Labs.
  
  **Institution-to-institution exchange.** If the receiving institution is regulated and asks for Travel Rule data, the information goes directly between the two compliance systems. It never appears on the public chain.
  
  **Identity shared, amount kept private.** The amount stays encrypted on-chain from start to finish. The Travel Rule concerns who is party to a payment, not its size, so Glade keeps those two things separate. Compliance data moves through compliance channels, and the ledger never sees a plaintext amount.
  
  ---
  
  ## What can trigger additional review
  
  - A payment larger than the limit for your verification level
  - A payment sent to or received from an address that sanctions or risk screening has flagged
  - Patterns that resemble structuring, for example several payments landing just under a reporting threshold
  
  Flagged payments may be held while someone reviews them by hand. You'll receive an in-app notice if this happens to one of yours.
  
  ---
  
  ## Related pages
  
  - [Regulation](regulation.md)
  - [Payment receipts](../confidentiality/payment-receipts.md)
  
