# 🔐 Password Manager Security Research

This project compares popular password managers from a security perspective.

## 🔎 Password Managers

The following password managers are included in this research:

- Bitwarden
- KeePass 2
- 1Password
- Proton Pass

## 🎯 Research Areas

For each password manager, the project examines:

- Password storage
- Encryption methods
- Key Derivation Functions (KDF)
- Multi-Factor Authentication (MFA)
- Passkey support
- Open-source availability
- Local or cloud storage
- Security audits
- Known vulnerabilities and incidents
- Privacy and zero-knowledge architecture

## 📊 Security Comparison

| Password Manager | Storage | Encryption | KDF | Open Source | MFA / 2FA |
|---|---|---|---|---|---|
| Bitwarden | Cloud / Self-hosted | AES-256 | PBKDF2 / Argon2id | ✅ Yes | ✅ Yes |
| KeePass 2 | Local `.kdbx` | AES-256 / ChaCha20 | AES-KDF / Argon2 | ✅ Yes | 🔑 Key file |
| 1Password | Cloud | AES-GCM-256 | PBKDF2-HMAC-SHA256 | ❌ No | ✅ Yes |
| Proton Pass | Cloud | AES-256 | Password-based KDF | 🟡 Client apps | ✅ Yes |

## 📁 Research

Detailed research for each password manager can be found in the `research/` directory:

- [Bitwarden Security Research](research/bitwarden.md)
- [KeePass 2 Security Research](research/keepass2.md)
- [1Password Security Research](research/1password.md)
- [Proton Pass Security Research](research/proton-pass.md)

## 📝 Conclusion

Each password manager uses a different security model. KeePass 2 focuses on local storage, while Bitwarden, 1Password, and Proton Pass provide encrypted cloud-based synchronization.

A secure password manager depends on more than encryption alone. Key derivation, authentication, software implementation, security audits, and user practices are also important.
