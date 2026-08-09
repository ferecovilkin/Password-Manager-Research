# Bitwarden Security Research

## Overview

Bitwarden is an open-source password manager that uses end-to-end encryption to protect user vault data.

## Where are passwords stored?

Bitwarden encrypts vault data on the user's device before syncing it to its cloud servers. Passwords are not sent to the server in plaintext.

### Source

- [Bitwarden — Data Storage](https://bitwarden.com/help/data-storage/)

## How is the vault encrypted?

Bitwarden uses AES-CBC 256-bit encryption. Encryption happens locally before vault data is sent to Bitwarden's servers.

### Source

- [Bitwarden — Encryption](https://bitwarden.com/help/what-encryption-is-used/)

## How is the master password protected?

Bitwarden does not store the user's master password. It is used to derive the cryptographic keys required to protect and unlock the vault.

### Sources

- [Bitwarden — Security Whitepaper](https://bitwarden.com/help/bitwarden-security-white-paper/)
- [Bitwarden — Security FAQs](https://bitwarden.com/help/security-faqs/)

## What KDF does Bitwarden use?

Bitwarden supports PBKDF2-SHA256 and Argon2id for key derivation. These make password guessing and brute-force attacks more expensive.

### Source

- [Bitwarden — KDF Algorithms](https://bitwarden.com/help/kdf-algorithms/)

## Does Bitwarden support MFA and passkeys?

Yes. Bitwarden supports two-step login including FIDO2 WebAuthn security keys. It also supports storing and using passkeys.

### Sources

- [Bitwarden — FIDO2 WebAuthn](https://bitwarden.com/help/setup-two-step-login-fido/)
- [Bitwarden — Passkeys](https://bitwarden.com/help/login-with-passkeys/)

## Is Bitwarden open source?

Yes. Bitwarden publishes its source code publicly on GitHub, including its server and client projects.

### Source

- [Bitwarden — Official GitHub](https://github.com/bitwarden)

## Security Audits and Incidents

Bitwarden undergoes third-party security assessments and independent security research. These reviews help identify weaknesses and improve the security of the platform.

### Sources

- [Bitwarden — Third-Party Security Audits](https://bitwarden.com/blog/third-party-security-audit/)
- [Bitwarden — ETH Zurich Cryptography Audit](https://bitwarden.com/blog/security-through-transparency-eth-zurich-audits-bitwarden-cryptography/)
