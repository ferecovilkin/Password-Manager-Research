# Proton Pass Security Research

## Overview

Proton Pass is a password manager developed by Proton for securely storing passwords and other login information.

## Questions

1. Where and how does Proton Pass store passwords?
2. How is the vault encrypted?
3. How is the account password protected?
4. What key derivation method does Proton Pass use?
5. Does Proton Pass support MFA and passkeys?
6. Is Proton Pass open source?
7. What security audits, vulnerabilities, or incidents are known?
## Where does Proton Pass store passwords?

Proton Pass encrypts vault data on the user's device before it is synced to Proton's servers. The servers store encrypted data and cannot access the plaintext contents of the vault.

### Source

- Proton Pass Security Documentation
