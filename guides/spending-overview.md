  # Spending overview
  
  This page turns the payment history of your accounts, including your agents, into a picture of where your money actually goes. The underlying data remains private to you. What you gain is the ability to spot patterns.
  
  ---
  
  ## Choosing the period
  
  One control at the top sets the period for the whole page: **7d**, **30d** or **90d**. Changing it recalculates every chart and total, as well as the comparison against the previous period of the same length.
  
  ---
  
  ## Headline figures
  
  | Figure | How it's worked out |
  |---|---|
  | Total transfers | The count of payments in the selected period |
  | Total volume | The sum of those payments |
  | Avg transfer amount | Total volume divided by the number of payments |
  | Settled rate | The percentage of payments whose final state was `Settled` |
  
  Next to each figure is the change from the period immediately before. On the 7-day setting, for example, this week is measured against last week. When the previous period had no activity, the change is left blank on purpose, because a percentage calculated from nothing would be misleading.
  
  ---
  
  ## Transfers per day
  
  This bar chart counts the payments sent on each day of the period. On the 90-day setting, the axis labels are thinned out so they don't overlap. Hover over a bar to get the precise count and volume for that day.
  
  ---
  
  ## Volume by account
  
  Here the total volume is split across every account you own, with human and agent accounts shown together. It's the quickest way to check whether one particular agent is behind a rise in spending.
  
  ---
  
  ## Volume by privacy layer
  
  This view shows how much volume settled under each of the three layers:
  
  - **Confidential**, the default unless you pick something else
  - **Shielded**
  - **Public**
  
  To understand what each layer means on-chain, see [Hidden amounts](../confidentiality/hidden-amounts.md).
  
  ---
  
  ## Activity by time of day
  
  A heatmap lays out days of the week against hours of the day, shaded by how much happened in each slot. It's particularly useful for checking agent behavior. An agent restricted to certain hours appears as a bright strip, and a scheduled job that runs when it should leaves a clear, regular mark.
  
  ---
  
  ## Where the data comes from
  
  Everything here is drawn from payments on accounts you own. Nobody else's activity is mixed in, and the page has no effect on what is visible on-chain. It simply presents records that were already yours.
  
  ---
  
  ## Related guides
  
  - [History](history.md)
  - [Agent accounts](../agents/agent-accounts.md)
  
