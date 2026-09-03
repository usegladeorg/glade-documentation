  # Send and receive
  
  Paying someone on Glade should feel about as involved as sending a message. Under the surface, each transfer is backed by a zero-knowledge proof and settled on Robinhood Chain. From where you sit, you pick a person, enter an amount and approve.
  
  ---
  
  ## How to send money
  
  ### Pick who you're paying
  
  Glade accepts four kinds of recipient:
  
  | Recipient | When to use it |
  |---|---|
  | A handle (for example `@maria.glade`) | The normal way to pay someone |
  | A QR code | Scan it in person, or load it from an image you've saved |
  | A request link | When someone has sent you a link asking for payment |
  | A raw EVM address (`0x...`) | Unusual cases, or wallets that don't use Glade |
  
  ### Set the amount and an optional note
  
  Notes are optional. When you add one, it's encrypted so that only you and the recipient can read it, and it is never written on-chain in plain text.
  
  ### Approve the payment
  
  Check the recipient and amount one more time. Then confirm with your device's biometric prompt, which uses the passkey from signup. Your device builds the proof and submits it to Robinhood Chain directly, so the key, the proof and the hardware never leave your control.
  
  ### See it land
  
  Settlement takes roughly 100 milliseconds, after which the payment appears in your feed and the recipient's. That's quicker than tapping a card, and it's private by default.
  
  Sending to a raw EVM address also settles on-chain. The difference is that the transfer only stays confidential when the receiving wallet supports Glade's confidential token contracts.
  
  ---
  
  ## How to get paid
  
  Receiving requires no action from you. Payments made to your handle, to your address or against one of your requests arrive on their own and appear in your feed.
  
  ### Asking for a specific amount
  
  To create a request, open **Send/Receive → Request** and then:
  
  1. Enter an amount, or leave the field blank to let the payer decide.
  2. Write a memo saying what the money is for.
  3. Share the link or QR code that Glade generates.
  
  The link opens in any ordinary browser, including for people who have never used Glade. Someone paying for the first time is walked through opening an account first, so a request also works as an invitation.
  
  ---
  
  ## Paying a wallet outside Glade
  
  Some addresses aren't set up for confidential transfers. If you try to send USDG to one, Glade stops and tells you the payment will go out as a regular public ERC-20 transfer. That warning always comes before you confirm, so you never lose privacy without knowing it.
  
  ---
  
  ## What it costs
  
  Glade charges nothing for transfers while the beta runs. You do pay Robinhood Chain gas, which is typically a small fraction of a cent and comes out of your ETH float automatically.
  
  ---
  
  ## Related guides
  
  - [Glade names](glade-names.md)
  - [History](history.md)
  
