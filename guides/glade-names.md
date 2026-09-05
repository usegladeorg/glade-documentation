  # Glade names
  
  A Glade name (your handle, such as `@yourname.glade`) is a readable stand-in for your account. Instead of copying a long EVM address and hoping they got every character right, people can pay you by name.
  
  ---
  
  ## Rules for choosing a name
  
  You claim a name while signing up. Later, you can move to another one under **Settings → Handle**, provided nobody else holds it.
  
  | Rule | Detail |
  |---|---|
  | Length | Between 3 and 20 characters |
  | Allowed characters | Letters, numbers and underscores only |
  | Capitalization | Ignored when matching names, but kept exactly as you typed it for display |
  
  ---
  
  ## What happens when someone pays your name
  
  Glade stores an off-chain mapping from your name to your public Robinhood Chain address. A payment to a name goes through three stages:
  
  1. The app finds the address that your name points to.
  2. A transfer is built and signed as usual, sent to that actual Robinhood Chain account.
  3. Only the transfer reaches the chain. The name itself is never recorded there; what settles is a plain address-to-address payment.
  
  Because the name is only used for lookup, it doesn't introduce a new party you need to trust. The payment carries exactly the protections described in [Hidden amounts](../confidentiality/hidden-amounts.md). The name makes things easier to use, and the cryptography underneath is unchanged.
  
  ---
  
  ## Names for agents
  
  Agent accounts are named underneath the owner's handle, in the form `@yourname/agent-name`. This matters because it should always be obvious when software is moving money. The nested name tells the person you're paying, and you when you review your feed, that an autonomous agent sent the payment rather than a human. Agent accounts are covered in detail in [Agent accounts](../agents/agent-accounts.md).
  
  ---
  
  ## Changing your name
  
  After you switch, your old name is held for a short period and then released for anyone to claim. Any request link built on the old name stops resolving at that point.
  
  Your Robinhood Chain address stays the same through a name change. Anything tied directly to that address, including your transaction history, carries on unaffected. The label can change, but the on-chain record can't.
  
  ---
  
  ## Related guides
  
  - [Send and receive](send-and-receive.md)
  - [History](history.md)
  
