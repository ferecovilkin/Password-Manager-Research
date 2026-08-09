# Bitwarden Security Research

## Overview

Bitwarden is a password manager that I am analyzing as part of this project.

## Questions

1. Where and how does Bitwarden store user passwords?
2. How is the password vault encrypted?
3. How is the master password protected?
4. What KDF does Bitwarden use?
5. Does Bitwarden support MFA and passkeys?
6. Is Bitwarden open source?
7. Has Bitwarden had any important security vulnerabilities or audits?

## Notes

## Where and how does Bitwarden store user passwords?

Bitwarden encrypts a user's vault data on the device before it is sent to the server. The encrypted vault is then synced to Bitwarden's cloud servers. This means that passwords and other vault data are not sent to the server in plaintext.

### Source

- Bitwarden Documentation — Data Storage

  ## How is the password vault encrypted?

Bitwarden uses AES-CBC 256-bit encryption to protect vault data. The encryption happens locally on the user's device before the data is sent to Bitwarden's servers. Because Bitwarden uses a zero-knowledge model, the company cannot access the unencrypted contents of the vault.

### Source

- Bitwarden Documentation — What encryption is used?

## How is the password vault encrypted?

Bitwarden uses AES-CBC 256-bit encryption to protect vault data. The encryption happens locally on the user's device before the data is sent to Bitwarden's servers. Because Bitwarden uses a zero-knowledge model, the company cannot access the unencrypted contents of the vault.

### Source

- Bitwarden Documentation — What encryption is used?
## How is the master password protected?

Bitwarden does not store the user's master password on its servers. The master password is processed on the user's device and is used to derive the cryptographic keys needed to protect the vault.

Because Bitwarden follows a zero-knowledge model, it does not have access to the user's master password or the unencrypted vault data.

### Sources

- Bitwarden Security Whitepaper
- Bitwarden Security FAQs
