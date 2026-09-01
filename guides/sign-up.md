  # Sign up
  
  Opening a Glade account takes a few minutes and assumes no prior knowledge of crypto. You won't be asked to write down a recovery phrase or buy a hardware wallet. Even so, the account is genuinely self-custodied: the keys belong to you, packaged in a way that works for ordinary people.
  
  ---
  
  ## Before you start
  
  Have these ready:
  
  | Item | Notes |
  |---|---|
  | A device that supports passkeys | Face ID, Touch ID and Windows Hello all work, as does a hardware security key |
  | An email address | This becomes your sign-in and contact address |
  | Government-issued ID | Needed for identity verification |
  
  ---
  
  ## Setting up your account
  
  ### Step 1: Create your login
  
  Type in your email, then make a passkey on the device you're using. Glade derives your keypair from that passkey. The result is cryptographic self-custody with nothing to memorize and nothing to store on paper.
  
  ### Step 2: Confirm who you are
  
  Identity checks happen at account opening because Glade operates inside the GENIUS Act framework. That arrangement keeps your activity hidden from the public while still meeting legal accountability requirements. The verification provider will request two things:
  
  - A clear picture of an ID issued by your government
  - A liveness check (a brief selfie video)
  
  Basic verification comes with standard limits. If you need more room, enhanced verification raises those limits in exchange for additional documents. It's available on Personal and Business accounts alike.
  
  ### Step 3: Pick your name
  
  Choose a handle, such as `@yourname.glade`. It's how other people find and pay you, so no one needs to copy your raw EVM address. The rules for choosing one are in [Glade names](glade-names.md).
  
  ### Step 4: Add money
  
  Move USDG in from an exchange or another wallet. Where it's supported in your region, a linked bank transfer is another option. Gas is paid in ETH, but Glade keeps a small ETH balance topped up on your behalf, so you never have to buy or manage it.
  
  ---
  
  ## What happens on-chain when you sign up
  
  A few real pieces of infrastructure are created for you behind the scenes:
  
  1. **A smart account on Robinhood Chain.** Its address is derived from your passkey.
  2. **A confidential USDG token account** inside Glade's contracts. This is the piece that makes encrypted transfers possible.
  3. **An off-chain profile record** tying your handle to your public key. It exists purely for lookups and display.
  
  At this point your account has no balance and no transaction history. Privacy is the default from day one, so the very first transfer you make is encrypted, exactly like every one after it. There's no setting to switch on.
  
  ---
  
  ## Which account type you get
  
  New accounts are Personal by default. If you're signing up for a company, select Business during signup instead; it adds shared access and higher limits. For a side-by-side look at Personal, Business and Agent accounts, see [Account kinds](../start/account-kinds.md).
  
  ---
  
  ## Next steps
  
  - [Send and receive](send-and-receive.md)
  - [Glade names](glade-names.md)
  
