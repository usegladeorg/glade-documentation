  # Spending rules
  
  Each agent answers to its parent account through a spend policy. Having a policy is why you can trust software with real money: the agent can genuinely spend, and none of your own authority over the account is given up in the process.
  
  ## Rules you can set
  
  | Rule | Effect |
  |---|---|
  | Daily limit | The most USDG the agent may spend in any rolling 24-hour window. |
  | Per-transaction limit | The largest amount allowed in one payment. |
  | Allowed recipients | The addresses, handles or domains (for x402) the agent may pay. Anything else is off limits. |
  | Asset restrictions | Which assets the agent may spend. Only USDG is allowed unless you change it; bridged USDC and ETH can be switched on. |
  | Time windows | The hours or days when the agent is allowed to transact. |
  | Approval threshold | An amount above which a person must explicitly approve the payment before it goes through. |
  
  ## Setting up a policy
  
  In the parent dashboard, open **Agents → [agent name] → Spend Policy**. To do it programmatically, use the endpoints in the [agents API](../reference/agents-api.md).
  
  Policies can be changed whenever you like. A change only affects transactions made after it is saved. Payments that have already settled stay as they are.
  
  ## How rules are enforced
  
  Most spend controls look at a payment after it has been made. Glade checks it before a signature even exists. As the agent signs, it compares the proposed payment with the policy in effect at that moment. If even one rule is broken, the transaction is never built and nothing reaches the chain. So you will not see an agent send an out-of-policy payment that gets quietly rejected later. That payment is simply never signed.
  
  ## When a payment needs approval
  
  If a payment is larger than your threshold, the agent prepares the transaction, puts it on hold and notifies the parent account. Someone looks over the amount, who it is going to and any context the agent supplied, then approves or declines it.
  
  | Outcome | What happens |
  |---|---|
  | Approved | The payment is signed and sent immediately. |
  | Declined | The payment is discarded. Nothing is submitted and no money moves. |
  | No response | The request expires after a configurable period (24 hours by default) and is treated as declined. |
  
  The threshold sets how much freedom the agent has. Put it at zero and you will review every single payment. Set it high for an agent you are comfortable leaving alone with routine, small purchases.
  
  ## A sample policy
  
  
