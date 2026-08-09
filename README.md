# 🔐 Password Manager Security Research

A security-focused comparison of popular password managers and the methods they use to protect user credentials.

## 🔎 Password Managers

This project focuses on four popular password managers:

- Bitwarden
- KeePass 2
- 1Password
- Proton Pass

## 🎯 Research Areas

Each password manager is examined based on:

- Password storage
- Encryption methods
- Key Derivation Functions (KDF)
- Multi-Factor Authentication (MFA)
- Passkey support
- Open-source availability
- Local vs. cloud storage
- Security audits
- Known vulnerabilities and incidents
- Zero-knowledge architecture

## 📊 Security Comparison

| Password Manager | Storage | Encryption | KDF | Open Source | MFA / 2FA |
|---|---|---|---|---|---|
| Bitwarden | Cloud / Self-hosted | AES-256 | PBKDF2 / Argon2id | ✅ Yes | ✅ Yes |
| KeePass 2 | Local `.kdbx` | AES-256 / ChaCha20 | AES-KDF / Argon2 | ✅ Yes | 🔑 Key file |
| 1Password | Cloud | AES-GCM-256 | PBKDF2-HMAC-SHA256 | ❌ No | ✅ Yes |
| Proton Pass | Cloud | AES-256 | Password-based KDF | 🟡 Client apps | ✅ Yes |

## 📁 Detailed Research

More detailed notes and official sources are available for each password manager:

- [Bitwarden Security Research](research/bitwarden.md)
- [KeePass 2 Security Research](research/keepass2.md)
- [1Password Security Research](research/1password.md)
- [Proton Pass Security Research](research/proton-pass.md)

## 🔍 Key Findings

The research shows that these password managers use different approaches to credential security.

**KeePass 2** follows a local-first model where the encrypted database remains under the user's control.

**Bitwarden** provides an open-source, zero-knowledge architecture with cloud synchronization and self-hosting support.

**1Password** uses a cloud-based security model that combines the account password with a unique Secret Key.

**Proton Pass** uses end-to-end encryption and provides open-source client applications.

## 📝 Conclusion

There is no single feature that determines whether a password manager is secure.

Encryption, key derivation, authentication, software implementation, security audits, and user practices all contribute to overall security.

The main difference between these password managers is how they balance security, storage, transparency, and convenience.

## ⚠️ Disclaimer

This project was created for educational and cybersecurity research purposes.

The information is based primarily on publicly available official documentation and security reports. Security features may change over time, so the original sources should be checked for the latest information.
