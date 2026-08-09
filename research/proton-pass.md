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
7. What security audits or vulnerabilities are known?

## Where does Proton Pass store passwords?

Proton Pass encrypts vault data on the user's device before it is synced to Proton's servers. The servers store encrypted data and cannot access the plaintext contents of the vault.

### Source

- [Proton Pass — Security](https://proton.me/pass/security)

## How is the vault encrypted?

Proton Pass uses end-to-end encryption to protect vault data. Each vault uses a unique 256-bit AES key, and encryption and decryption happen on the user's device.

### Source

- [Proton Pass — Vault Encryption](https://proton.me/support/pass-vault)

## How is the account password protected?

Proton uses a zero-knowledge architecture, so the account password is not stored in plaintext by Proton. It is used as part of the process that protects the cryptographic keys needed to access encrypted data.

### Source

- [Proton Pass — Security Model](https://proton.me/blog/proton-pass-security-model)

## What key derivation method does Proton Pass use?

Proton uses password-based key derivation as part of its account security and encryption architecture. The derived keys are used within Proton's zero-knowledge encryption model.

### Source

- [Proton Pass — Security](https://proton.me/pass/security)

## Does Proton Pass support MFA and passkeys?

Yes. Proton Pass supports passkeys and can create, store, and use them for supported accounts. Proton accounts can also be protected with two-factor authentication.

### Sources

- [Proton Pass — Passkeys](https://proton.me/pass/passkeys)
- [Proton — Two-Factor Authentication](https://proton.me/support/two-factor-authentication-2fa)

## Is Proton Pass open source?

Yes. Proton Pass client applications are open source, allowing researchers and developers to inspect their code.

### Source

- [Proton — Proton Pass Open Source](https://proton.me/blog/pass-open-source-security-audit)

## Security Audits and Vulnerabilities

Proton Pass has undergone independent security audits by firms including Cure53 and Recurity Labs. These audits identified security issues that Proton addressed through updates.

### Sources

- [Proton Pass — 2026 Security Audit](https://proton.me/business/blog/proton-pass-audit-2026)
- [Proton Pass — Open Source and Security Audit](https://proton.me/blog/pass-open-source-security-audit)
