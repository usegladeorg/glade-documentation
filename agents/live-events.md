  # Live events
  
  Whenever a payment touches your account or one of its agents, you hear about it straight away. Dashboards, parent apps and monitoring tools can stay current from the moment money moves, without polling and without a delay.
  
  ## Subscribing to events
  
  You can create a subscription under **Dashboard → Developer → Webhooks** or through the API. Either way, the steps are the same:
  
  1. Give Glade an HTTPS endpoint that accepts `POST` requests.
  2. Choose which event types should be sent to it.
  3. Save the signing secret. Glade signs every payload with an HMAC using this secret, and you will only see it once, at the moment the subscription is created.
  
  Before your code acts on a request body, check the `X-Glade-Signature` header against that secret.
  
  ## Events you can receive
  
  | Event | Sent when |
  |---|---|
  | `transfer.initiated` | A payment has been submitted and is awaiting confirmation. |
  | `transfer.confirmed` | A payment has settled on-chain. |
  | `transfer.failed` | A payment did not settle. |
  | `agent.transaction.pending_approval` | An agent's payment exceeded its approval threshold. |
  | `agent.transaction.approved` | Someone approved a held agent payment. |
  | `agent.transaction.rejected` | Someone declined a held agent payment. |
  | `agent.policy.updated` | The spend policy on one of your agents changed. |
  
  ## What a payload looks like
  
  
