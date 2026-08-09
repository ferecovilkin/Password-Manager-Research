# 1Password Security Research

## Overview

1Password is a cloud-based password manager designed to securely store passwords and other sensitive information.

## Questions

1. Where and how does 1Password store passwords?
2. How is the vault encrypted?
3. How is the account password protected?
4. What is the Secret Key?
5. Does 1Password support MFA and passkeys?
6. Is 1Password open source?
7. What security audits, vulnerabilities, or incidents are known?
   
## Where does 1Password store passwords?

1Password encrypts vault data on the user's device before it is synced to the cloud. The servers store encrypted vault data, while encryption and decryption happen on the user's device.

### Source

- 1Password Security Documentation
  
## How is the vault encrypted?

1Password uses AES-GCM-256 encryption to protect vault data. The data is encrypted locally on the user's device before being sent to 1Password's servers.

### Source

- 1Password Security Documentation
