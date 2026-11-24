# Security

Never commit an API key, token, password, or other secret.

This repository is public. Your company's config repository is private, and the same rule applies there.

- Request the Theory config service key from Theory Network, then store it in a vault.
- Bots receive the vault secret's name (`config_service_key_secret`). The key stays out of repositories, bot memory, and chat.
- Keep the key out of `starter-prompt.md`, `context.example.md`, pull requests, and config files.
- If a key is committed or pasted where other people can see it, ask Theory Network to revoke it and issue a new one. Removing the file afterward leaves the old key in git history.

To report a secret exposure or another security issue, use the Theory Network contact in the [README](README.md) once it is published. Until then, reach Andre directly.
