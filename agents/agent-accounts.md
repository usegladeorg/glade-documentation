  # Agent accounts
  
  An agent on Glade has an account of its own. It is not a person's login with an API key and a webhook attached to the side. The agent holds its own wallet, has its own identity and accumulates its own payment history, and its owner decides the boundaries it works within. Agent accounts were planned for software from the start rather than adapted from accounts meant for people.
  
  ## What comes with an agent account
  
  Creating an agent account sets up four things:
  
  | Component | Details |
  |---|---|
  | Smart account | An ERC-4337 smart account on Robinhood Chain. Its signing key is separate from the one the parent uses. |
  | Agent ID | A name under the parent's namespace, in the form `@yourname/agent-name`. |
  | Encrypted balance | A balance of its own, held in Glade's confidential token contracts. |
  | Payment record | A log of the agent's payments that shows up in the parent's feed as they happen. |
  
  With this in place, the agent can hold USDG, accept funding from its parent and choose for itself when to make a payment. That freedom is real, but it only extends as far as the limits the owner has set.
  
  ## From task to settled payment
  
  
