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
