# Nexus

Nexus is a Grok Bot team for your company, run by an Orchestrator bot.

The Orchestrator is the bot that sets the team up and keeps it running. People talk to it, and it routes work to the rest of the team. It keeps every bot's instructions in sync with Theory Network, and it is the only bot that edits your company's configuration repository.

This repository is the public starting point. You copy a short bootstrap prompt from here, request an API key from Theory Network, and the Orchestrator takes the rest of setup from the Theory config service.

## How it works

**A hosted service renders your bots.** Theory Network runs the Theory config service. Your company has an API key. With that key, the service renders the bot instructions your company is licensed for and returns the onboarding questions for your company. The master templates stay in Theory Network's private `nexus-core` repository. Companies receive finished configs for their own team.

**Your config and memory live in a private repo.** Rendered bot configs, company values, and product memory live in a private repository. The default is `theory-network/nexus-client` (Theory Network and the companies it manages). A company that runs its own team can use its own private repository with the same layout. The API key stays in a vault. The repository stores only the name of that secret.

**Layouts are sized to your company.** Work is organized into departments. A few bots are fixed: the same infrastructure bots in every layout, including the Orchestrator. The rest are bundles of capabilities. A layout decides how those capabilities are grouped into bots:

- **Lean** — a few broad bots, for one person or a very small company.
- **Standard** — department bots, for a small team.
- **Split** — narrower bots, for a larger or busier company.

A company can mix layouts by department (for example lean overall, with one department at standard). The Orchestrator suggests a layout from your company size and license. You can change it later.

**Chat is optional.** People can reach the team from Slack or Microsoft Teams, or stay entirely in Grok Bot. You can add or remove chat later.

## Get started

1. **Request an API key** from Theory Network.
   Contact: `[PLACEHOLDER: Andre — add how to reach Theory Network for an API key]`.
   Theory Network issues the key and sends the config service address with it.
2. **Save the key in your vault.** Choose a secret name (for example `nexus-config-service-key`). You will give the Orchestrator that name only. See [SECURITY.md](SECURITY.md).
3. **Fill in a company brief** from [context.example.md](context.example.md). Keep your copy private. It gives onboarding a head start.
4. **Create an Orchestrator bot** in Grok Bot and paste in [starter-prompt.md](starter-prompt.md).
5. **Confirm the four bootstrap inputs** it asks for. It then checks the key with the Theory config service and follows the onboarding steps the service returns.

### Bootstrap defaults

| Input | What it is | Default |
| --- | --- | --- |
| `config_service_url` | Address of the Theory config service | Sent with your API key. A standing default will be published in this table when Theory Network chooses one. |
| `config_service_key_secret` | Name of the vault secret that holds the API key | You choose the name. The value stored in the repo is that name. |
| `client_repo` | Private repository for this company's configs and memory | `theory-network/nexus-client` |
| `context_file_path` | Human's default company and product context on the shared Grok Bot computer. Work queues live next to it. | `/home/box/team-context/current.yaml` |

## In this repository

| File | Purpose |
| --- | --- |
| [starter-prompt.md](starter-prompt.md) | Bootstrap prompt to paste into the Orchestrator |
| [context.example.md](context.example.md) | Example company brief to fill in before onboarding |
| [SECURITY.md](SECURITY.md) | Never commit API keys |
| [LICENSE](LICENSE) | License not chosen yet |

Master templates, capability definitions, and the full Orchestrator prompt stay in the private `nexus-core` repository. The config service delivers finished configs from there. This public repo ships only the files above.
