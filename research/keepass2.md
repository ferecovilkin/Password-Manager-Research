# KeePass 2 Security Research

## Overview

KeePass 2 is an open-source password manager that stores passwords in a local encrypted database.

## Questions

1. Where and how does KeePass 2 store passwords?
2. How is the database encrypted?
3. How is the master password protected?
4. What KDF does KeePass 2 use?
5. Does KeePass 2 support two-factor protection?
6. Is KeePass 2 open source?
7. What security issues are known?

## Where does KeePass 2 store passwords?

KeePass 2 stores passwords locally in an encrypted `.kdbx` database file. Unlike cloud-based password managers, KeePass does not require a central server to store the vault.

### Source

- [KeePass — Features](https://keepass.info/features.html)

## How is the database encrypted?

KeePass 2 encrypts its database using strong symmetric encryption such as AES-256 or ChaCha20. It also uses key derivation methods such as Argon2 or AES-KDF to make brute-force attacks more difficult.

### Source

- [KeePass — Security](https://keepass.info/help/base/security.html)

## How is the master password protected?

KeePass protects the database using a master key. This key can be based on a master password, a key file, a Windows user account, or a combination of them.

KeePass also uses protection against brute-force and dictionary attacks.

### Source

- [KeePass — Master Key](https://keepass.info/help/base/keys.html)

## What KDF does KeePass 2 use?

KeePass 2 supports AES-KDF and Argon2 for key derivation. These functions make password guessing and brute-force attacks more difficult.

### Source

- [KeePass — Security](https://keepass.info/help/base/security.html)

## Does KeePass 2 support two-factor protection?

KeePass 2 can combine a master password with a key file for two-factor protection. Both components are required to open the database.

### Source

- [KeePass — Master Key](https://keepass.info/help/base/keys.html)

## Is KeePass 2 open source?

Yes. KeePass 2 is free and open-source software. Its source code is publicly available and the project is licensed under the GNU GPL.

### Source

- [KeePass — Official Website](https://keepass.info/)

## Security Issues

KeePass has had several reported security issues over time. Some older issues, including database header authentication problems, were addressed in later versions.

KeePass also documents known security concerns and their current status on its official website.

### Source

- [KeePass — Security Issues](https://keepass.info/help/kb/sec_issues.html)
