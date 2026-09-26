  # Pay per request with x402
  
  x402 is an open protocol for payments between machines. It is built on HTTP status 402 Payment Required, a code that sat mostly unused for a long time. Glade supports x402 natively, which means an agent account can pay for API calls, compute and other services with no card, no OAuth flow and no prepaid balance to keep topped up. A payment takes about as long as an HTTP round trip.
  
  Robinhood Chain was designed for exactly this kind of user; its stated goal is to let agents trade, swap and pay. On that chain, x402 is the obvious way to handle payments. A service gets one standard way to state its price. An agent gets one standard way to pay it, inline, as part of the request it was making anyway.
  
  ## The payment flow
  
  
