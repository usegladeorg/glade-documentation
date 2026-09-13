  # Keys and restoring access
  
  Glade doesn't just promise self-custody. The system is built so that it couldn't work any other way. Keys are created on your device and stay there. Glade holds no copy and never handles them in unencrypted form, which means the account really is yours.
  
  ---
  
  ## Your two keypairs
  
  Each account uses two keypairs with separate responsibilities.
  
  | Keypair | Responsibility |
  |---|---|
  | **Signing key** | An ordinary EVM key (secp256k1), like the one in any Ethereum wallet. It controls your smart account and signs the transactions it sends. |
  | **Decryption key** | Unlocks your confidential token balance, so you can read your own amounts and look through your transaction history. |
  
  Both come from a single secret that your hardware generates when you sign up. Glade never receives either key unencrypted.
  
  ---
  
  ## Keys from your passkey
  
  Glade uses WebAuthn for onboarding, so there's no recovery phrase to copy onto paper. You hold full custody without a piece of paper you might misplace.
  
  1. You sign up with an email address and a passkey on your device. That can be Face ID, Touch ID, Windows Hello or a hardware security key.
  2. Your device runs a key derivation function over the passkey and generates your Glade keypair locally.
  3. The private key material is encrypted and kept in the secure enclave, or in your platform's equivalent.
  4. Glade only ever sees your public key and the transactions you sign.
  
  The most common way self-custody fails in practice is a seed phrase that gets written down and then lost. This setup avoids that. You give nothing up for it either, because you can still export the key at any time.
  
  ---
  
  ## Exporting the key
  
  Go to **Settings → Security → Export Key** whenever you want. Your Glade smart account is controlled by a standard Ethereum-style key, and Robinhood Chain is fully EVM-compatible, so the exported key works in any normal EVM wallet, including MetaMask, Rabby and Rainbow. Nothing ties you to Glade.
  
  Once exported, protecting that key is up to you. Whoever holds it controls the account.
  
  ---
  
  ## If you lose a device
  
  | Option | How it restores access |
  |---|---|
  | **Synced passkeys** | When your passkey is also on another device, or synced through a provider such as iCloud Keychain or Google Password Manager, signing in somewhere else gets you back in immediately. |
  | **Social recovery (post-beta)** | You nominate trusted contacts. Together, they can approve recovering your account. |
  | **Exported backup** | A key you exported earlier and stored safely restores the account on any device. |
  
  Each of these depends on your key material, and that's intentional. Glade has no reset button and can't let you back in itself, because it never held what that would require.
  
  ---
  
  ## Keys and privacy
  
  Your decryption key is also how you share or export data without going through anyone else. You are the only holder, so you're the only one who can see your history or prove a payment's contents to another party. One key, kept in one enclave, gives you both control and confidentiality. See [Payment receipts](payment-receipts.md) for more.
  
