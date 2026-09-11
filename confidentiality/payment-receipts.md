  # Payment receipts
  
  Keeping an amount private doesn't mean you can never prove it. Glade lets you reveal a single payment to a single person at a moment you choose. Everything else in your account stays closed.
  
  ---
  
  ## Disclosure proofs
  
  A disclosure proof reveals what one transaction was worth to whoever you send it to. You sign it with your account key, which lets the recipient confirm it really came from you and wasn't fabricated. You decide what it covers, and it reveals nothing outside that scope.
  
  ### When people use them
  
  - Showing a landlord, employer or vendor that a specific payment was made
  - Answering a question from a tax authority or auditor about one transaction
  - Meeting Travel Rule screening requirements with an institution on the other side of a payment (see [Identity checks](../trust/identity-checks.md))
  
  ### Generating one
  
  1. Open the payment in your history and choose **Generate disclosure**.
  2. Decide on the contents. You can share the amount on its own or the amount plus its memo.
  3. Glade produces a proof of that transaction's contents and signs it with your key.
  4. Pass the resulting link or exported file to the person who asked for it.
  
  Nothing around the payment leaks in the process. Your other transactions and balances are not part of the proof.
  
  ---
  
  ## Exporting your full history
  
  For bookkeeping or tax filing, you can export your decrypted history in one step.
  
  | | |
  |---|---|
  | Where to find it | **Settings → Export → Transaction History** |
  | Formats | CSV or JSON |
  | Contents | Decrypted amounts, timestamps, counterparties and memos |
  | Works with | Popular crypto tax tools such as Koinly, TokenTax and CoinTracker |
  
  The whole export runs on your device. Your key decrypts the records and the file is written locally. Glade's servers never get the decrypted file, and they have no means of getting it.
  
  ---
  
  ## Limits on what Glade can do
  
  - **No decrypting for third parties.** Glade cannot open your transactions for anyone else. A disclosure only exists if you create and sign it.
  - **No plaintext storage.** Your history is not kept in readable form on Glade's servers.
  - **No forged proofs.** A valid disclosure proof requires your private key. That is a property of the system, not a policy Glade has chosen to follow, so it still holds if Glade is pressured.
  
  ---
  
  ## The link to regulation
  
  Disclosure proofs are what make Glade's stance of confidentiality without anonymity workable. That stance is explained in [Regulation](../trust/regulation.md). Your identity is verified at sign-up and your address is public. Amounts stay sealed until you decide to reveal one, or until lawful process directed at you as the account holder requires it.
  
  ---
  
  ## Related pages
  
  - [Identity checks](../trust/identity-checks.md), for how accounts get verified
  - [Keys and restoring access](keys-and-restoring-access.md), for the key that ensures only you can disclose
  
