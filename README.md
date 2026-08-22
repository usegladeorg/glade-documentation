  ![Glade, a private bank for people and the agents working for them](https://useglade.org/images/og.jpg)
  
  # Glade documentation
  
  **Glade is private money for you and for the software that acts for you. Custody stays with you, settlement happens on Robinhood Chain, and the amount of each payment is readable only by the sender and the recipient.**
  
  ---
  
  ## Why Glade exists
  
  Most money today moves through one of two systems, and each gives something up. A bank keeps your ledger away from the public, but the bank itself sees all of it, as do its processors and whoever it decides to sell your spending data to. A public blockchain reverses the trade. Every entry can be audited, nothing is discreet, and anybody with an RPC endpoint can look up what you were paid.
  
  Glade doesn't accept either compromise. Payments settle on Robinhood Chain, which lets the network confirm that they happened, while the amounts remain encrypted end to end. The parties are visible and the sums are not. The key that unlocks your own numbers never leaves the device in your hand.
  
  The same account works for a freelancer who gets paid in USDG on a Tuesday afternoon and for a research agent that pays eleven cents for an inference call at 4am. Software gets a real wallet of its own, bounded by limits that its owner chooses, and everything it does appears in the same activity feed as your other payments.
  
  ---
  
  ## Glade next to the alternatives
  
  | | Glade | A typical crypto wallet | A high-street bank |
  |---|---|---|---|
  | Visibility of amounts | Stored encrypted on-chain | Public plaintext, readable by anyone indefinitely | Private from outsiders, but the bank sees them |
  | Who holds the keys | You do, on your own device | You do | The bank does |
  | Time to settle | Under a second | Under a second | A few days |
  | Software holding an account | Dedicated wallets with limits that are enforced | An API bolted onto a human's account | Not available |
  | Sharing payment details | You generate a proof for a single transaction | There's nothing to share because it's all public | Decided by the bank |
  | Getting started | Passkey, then an identity check | Writing down a twelve-word phrase | A form, then a wait |
  
  ---
  
  ## The technology underneath
  
  Glade deploys its own confidential token contracts on Robinhood Chain, the AI-native Ethereum Layer 2 operated by Robinhood. Those contracts keep balances as ciphertext and require a zero-knowledge proof with every transfer. The addresses involved stay public. Combined with 100ms blocks and rollup-level fees, this gives you payments that are private and self-custodied, settle almost instantly, and cost little enough to use every day. No chain before it offered all of that at once.
  
  Balances are held in USDG, the Global Dollar issued by Paxos natively on Robinhood Chain. Bridged USDC is also accepted. Gas comes from a small ETH reserve that tops itself up automatically in the background, so once your account is set up, gas is not something you have to manage.
  
  ---
  
  ## Pick a starting point
  
  | If you want to... | Read |
  |---|---|
  | Follow a single transfer from start to finish | [Life of a payment](start/life-of-a-payment.md) |
  | Look after your own money | [Sign up](guides/sign-up.md) |
  | Hand an autonomous system a budget | [Agent accounts](agents/agent-accounts.md) |
  | Build Glade into your own product | [Authentication](reference/authentication.md) |
  | Study the cryptography in depth | [Hidden amounts](confidentiality/hidden-amounts.md) |
  
