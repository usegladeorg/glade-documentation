  # Preferences
  
  Preferences covers four areas: your profile, the wallet you've linked, any spending limits you set on yourself, and what happens to your data.
  
  ---
  
  ## Profile
  
  | Field | Details |
  |---|---|
  | **Handle** | Fixed once claimed; it can't be edited. See [Glade names](glade-names.md). |
  | **Display name** | Appears on your public profile. Change it whenever you like. |
  | **Email** | The address you registered with. Receipts and alerts are sent here. |
  
  ---
  
  ## Linked wallet
  
  Set or update the Robinhood Chain address Glade uses for payouts and on-chain activity. Glade validates the format before saving. An invalid address is refused immediately, rather than being accepted and failing at some later point.
  
  ---
  
  ## Limits you set for yourself
  
  | Setting | Effect |
  |---|---|
  | Daily limit | Once outgoing payments for the day reach this amount, further ones are blocked. Enter `0` to disable. |
  | Monthly limit | A hard ceiling for the calendar month. Enter `0` to disable. |
  | Require confirmation | Asks you to confirm again before any payment above $0.50. |
  | Auto top-up | Refills the primary account when its balance runs low. |
  
  These limits only affect your own account. Limits for an *agent* are a different mechanism entirely. They're defined through [Spending rules](../agents/spending-rules.md) and enforced on-chain, not saved as a preference. In other words, an agent's limits are hard constraints, while the settings above are yours to adjust.
  
  ---
  
  ## Run behavior
  
  | Setting | Effect |
  |---|---|
  | Stream results | Shows a payment's progress as it happens, rather than just its final state |
  | Save execution history | Keeps run outputs and receipts on your account for later review |
  | Share anonymised usage data | Optional product telemetry; content is never included |
  
  ---
  
  ## Exporting everything
  
  **Export all data** produces one JSON file with your accounts, payments, alerts, API keys and webhooks. It's a complete, portable copy of what you have on Glade.
  
  There's also a narrower export that covers payments only, described in [Payment receipts](../confidentiality/payment-receipts.md). Use **Export all data** when you want the whole snapshot. Use the payments export when an accountant or regulator specifically needs your decrypted payment history.
  
  ---
  
  ## Closing your account
  
  Requesting deletion signs you out straight away and queues your account and data for permanent removal within 30 days. Until that window ends, support can reverse the request. Once the 30 days are up, the deletion is final and nothing can be restored.
  
  ---
  
  ## Related guides
  
  - [Topping up](topping-up.md)
  - [Payment receipts](../confidentiality/payment-receipts.md)
  
