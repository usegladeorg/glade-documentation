  # Authentication
  
  The REST API uses a single bearer token for everything: accounts, transfers and agent wallets. Every request must carry an API key, and keys are issued from a Glade account.
  
  ---
  
  ## Generate a key
  
  Keys come from the **Developer** area of the dashboard.
  
  1. Sign in to Glade.
  2. Go to **Dashboard → Developer → API Keys**.
  3. Select **Generate New Key**.
  4. Label it so you can tell keys apart later. Something like `production`, `dev` or `internal-tool` works well.
  5. Copy it somewhere safe immediately. The key is shown only this one time.
  
  A key belongs to the account that generated it. Transfers sent with it are just as confidential as transfers sent from the app, so automating a payment does not cost you any privacy.
  
  ---
  
  ## Send the key with each request
  
  Put the key in the `Authorization` header:
  
  
