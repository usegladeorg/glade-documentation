  # Onchain contracts
  
  Balances and transfers in Glade live in a confidential token contract deployed on Robinhood Chain. It is an ERC-20 wrapper whose balances are encrypted, built along the lines of Zether. Because the EVM offers no native way to transfer value confidentially, Glade built this layer itself, published the source, and verified the deployed code on-chain.
  
  There is nothing running beside it. Glade keeps no private ledger and no internal record of who owns what, so reading the token contract tells you everything about how money moves.
  
  ---
  
  ## Storage inside the token contract
  
  `ConfidentialToken` wraps an ordinary ERC-20, which on Robinhood Chain is USDG. For every registered account it stores the balance as an ElGamal ciphertext over the alt_bn128 curve. Registration is a one-time call to `register` with the account's ElGamal public key. After that, the account's balance is one ciphertext made of two points:
  
  
