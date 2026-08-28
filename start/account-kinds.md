  # Account kinds
  
  Glade offers three account kinds, and they all sit on the same foundation: the same wallet infrastructure, the same confidential transfer engine and the same guarantees. Where they differ is in who controls the keys, who is allowed to approve which actions, and how much oversight sits on top.
  
  ## Which one fits
  
  | What you want to do | Choose |
  |---|---|
  | Send and receive USDG for yourself | Personal |
  | Run one balance that a team can see and use | Business |
  | Let software spend money inside limits you define | Agent |
  
  ---
  
  ## Personal
  
  This is the account for one person handling their own money.
  
  **What it does**
  - Holds USDG and ETH, and sends and receives confidential transfers
  - Gives you a `@handle`, so people can pay you without copying an address
  - Creates request links and QR codes on demand
  - Exports your decrypted history for tax season
  
  **How privacy works**
  - Encryption is on from the first transfer, and there's no toggle you could leave switched off
  - Nothing gets disclosed unless you generate a proof for that purpose
  
  ---
  
  ## Business
  
  This is the account for an organization in which several people need to see a single balance without any of them sharing a key.
  
  **What it does**
  - Everything a Personal account does
  - Several authorized signers, each with an assigned role
  - Higher default limits once enhanced verification has been completed
  - Bulk payouts for payroll and paying suppliers
  
  **How privacy works**
  - Confidentiality identical to a Personal account
  - Exports laid out so they import straight into accounting and tax software
  
  ---
  
  ## Agent
  
  This is a wallet built for software from the start, not adapted from one meant for a person.
  
  **What it does**
  - Gets a dedicated Robinhood Chain smart account and an Agent ID that lives under a parent (`@username/agent-name`)
  - Spends only within the parent's spend policy, which can set daily limits, approved counterparties, asset restrictions and operating hours
  - Speaks x402 out of the box, with no adapter needed
  - Mirrors every payment into the parent's feed as it happens
  
  **How privacy works**
  - Encrypted by default, exactly like a human-held account
  - The parent can add an approval step for any amount over a threshold they choose
  
  [Agent accounts](../agents/agent-accounts.md) walks through setting one up and keeping an eye on it.
  
  ---
  
  ## How agents relate to their parent
  
  An Agent account always has a parent, which must be a Personal or Business account. You create the agent from that parent, and the agent operates under a policy the parent is free to change whenever it likes. The agent can act on its own, but the final say stays with you.
  
