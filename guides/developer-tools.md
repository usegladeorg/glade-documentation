  # Developer tools
  
  The API Keys screen lets you issue credentials and set up webhook endpoints from inside the app, with no hand-written requests. Think of it as the point-and-click companion to the [authentication reference](../reference/authentication.md).
  
  ---
  
  ## Issuing an API key
  
  1. Click **+ New key**.
  2. Name it, for instance `Production`.
  3. Pick the environment it belongs to.
  
  | Environment | Key prefix | What it touches |
  |---|---|---|
  | Live | `hc_live_` | Real USDG and real transfers |
  | Test | `hc_test_` | Robinhood Chain testnet, so no real money |
  
  The full key appears a single time, right after you create it. Copy it before you close the panel. Glade keeps only a hash of the key, so neither you nor we can retrieve it later. Lost a key? Revoke it and issue another. This is deliberate, and it's how keys should be handled.
  
  ---
  
  ## Revoking an API key
  
  Press **Revoke** beside any active key. It stops working straight away and can't be reactivated; every request made with it from then on fails. The key remains in your list marked **Revoked**, which keeps your audit trail complete.
  
  ---
  
  ## Registering a webhook endpoint
  
  In the Webhooks section, choose **+ Add endpoint** and supply:
  
  - **A URL** using HTTPS, where deliveries will be sent
  - **The events** you want: any of `transfer.settled`, `transfer.failed`, `payment.received` and `policy.limit_reached`
  
  An endpoint only receives the event types you chose for it. There's no need to funnel everything through one endpoint. You can create as many as your systems need, say one that posts to Slack and another that feeds billing, each with its own event selection.
  
  ---
  
  ## Pausing or removing an endpoint
  
  Each endpoint can be set to **Active** or **Inactive**, or deleted outright.
  
  | Action | Effect |
  |---|---|
  | Set to Inactive | Deliveries stop, but the configuration is kept. Useful while you repair whatever receives them. |
  | Delete | The endpoint is gone for good. |
  
  ---
  
  ## Events and payloads
  
  This screen is limited to managing keys and endpoints. The full event list, payload shapes and signature verification steps live in [Live events](../agents/live-events.md) and the [Webhooks API](../reference/webhooks-api.md).
  
  ---
  
  ## Related pages
  
  - [Authentication](../reference/authentication.md)
  - [Live events](../agents/live-events.md)
  
