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
## What KDF does Bitwarden use?

Bitwarden supports two Key Derivation Functions (KDF): PBKDF2-SHA256 and Argon2id.

A KDF makes the master password harder to attack by increasing the computational cost of password guessing. PBKDF2 does this mainly through repeated iterations, while Argon2id also uses memory, which makes large-scale brute-force attacks more expensive.

Users can configure the KDF and its parameters in their Bitwarden account settings.

### Source

- Bitwarden Documentation — KDF Algorithms
## Does Bitwarden support MFA and passkeys?

Yes. Bitwarden supports multiple methods of two-step login, including FIDO2 WebAuthn.

FIDO2 WebAuthn can be used with hardware security keys and provides phishing-resistant authentication. Bitwarden also supports passkeys and can store them inside the encrypted vault for use when signing in to supported websites and services.

These features add an extra layer of protection against account takeover and phishing attacks.

### Sources

- Bitwarden Documentation — FIDO2 WebAuthn
- Bitwarden Documentation — Passkeys
## Is Bitwarden open source?

Yes. Bitwarden is open source, and its source code is publicly available on GitHub.

Important parts of the project are available in separate repositories. For example, the `server` repository contains backend and infrastructure code, while the `clients` repository contains the web app, browser extension, desktop app, and CLI code. Bitwarden also publishes separate repositories for its Android and iOS applications.

Being open source allows security researchers and developers to review the code, report security issues, and contribute to the project.

### Source

- Bitwarden Official GitHub Organization
## Security audits and known incidents

Bitwarden regularly undergoes third-party security assessments, including penetration testing and source code reviews. Security firms such as Cure53 have been involved in assessments of Bitwarden products.

Bitwarden has also been studied by independent security researchers. Researchers from ETH Zurich analyzed parts of Bitwarden's cryptographic design using a malicious-server threat model, and Bitwarden published information about the findings and resulting improvements.

In 2026, Bitwarden also reported a supply-chain security incident involving the npm distribution of its CLI package. According to the available reports, the incident affected the CLI distribution channel rather than representing a compromise of Bitwarden's main vault infrastructure.

These examples show that even security-focused and open-source software can have vulnerabilities or supply-chain risks, making independent audits and continuous security testing important.

### Sources

- Bitwarden — Third-Party Security Audits
- Bitwarden — ETH Zurich Cryptography Audit
- Bitwarden Security Whitepaper
