# .ssh

Extensable configuration template for your ~/.ssh/ directory on macOS and linux.

## Features:

- Automatically reads any `*.config` files in `~/.ssh/` for user configurations
- Automatically read default keys from `~/.ssh/idenntities`
- Protects `known_hosts` using HMAC
- Use Keychain for ssh-agent on macOS
- Enables verifiying SSHFP records with DNSSEC for hosts on the internet
- Read optional KRL/RevokedHostKeys file if available (in addition to `@revoked`)
- Uses a secure set of user-overridable defaults:
	- Only use identities over the internet
	- Disallow password authenticaion over the internet by default
	- Disallow insecure cipher and hash algos
- Some usability features:
	- Don't strictly check hosts on ephemeral networks, such as `168.254/16` link-local
	- Don't strictly check hosts on link-local, such as `fc*%%lo0` or `127/8`
	- Disable compression on LAN 
- Some optional extra features:
	- Warn when depreciated private keys are present



## Installation:

```bash
git clone https://github.com/stonegray/.ssh ~/.ssh

# Move any existing keys into identities folder:
mv ~/.ssh/id_* ~/.ssh/identities/
```

If you don't require updates and don't plan to contribute, you can remove `.git` after installation.



