# Company context (example)

Copy this file somewhere private and replace the sample answers with your own. Keep the copy out of the public `nexus-starter` repository. Leave API keys, passwords, and other secrets out of it; the key lives in a vault, and onboarding only needs the secret's name.

This brief is what you fill in before onboarding so the answers are ready. During setup the Orchestrator also keeps a short live context file on the shared Grok Bot computer (default path `/home/box/team-context/current.yaml`). That live file is only the human's current company and product. This page is the longer prep note.

Sample company: **Northwind Studio**. Replace every sample.

## Company

- **Name:** Northwind Studio
- **What you do, in a few sentences:** We design and build small software products for independent publishers.
- **Website:** https://example.com
- **Other docs worth reading** (links, or where they live): Pitch deck in the company drive. Brand notes in the team wiki.
- **About how many people work here:** 4
- **Owner** (name, and how to reach them in Grok Bot): Example Owner, owner@example.com

## Products

Add one block per product. Delete the samples you do not need.

### Harbor

- **Name:** Harbor
- **What it is:** A web app where publishers track manuscript submissions.
- **Public URL or repo, if any:** https://github.com/example/harbor
- **Who should approve releases:** Example Owner

### Field Notes

- **Name:** Field Notes
- **What it is:** A short newsletter for the same publishers.
- **Public URL or repo, if any:** https://example.com/field-notes
- **Who should approve releases:** Example Owner

## How you want to start

- **People and pace:** Four people, a few requests a week. The Orchestrator uses this, with your license, when it suggests a layout (lean, standard, or split).
- **Chat:** None for now. Slack or Microsoft Teams can be added later.
- **Private config repo:** `theory-network/nexus-client`, unless Theory Network gave you your own.
- **Vault secret name for the API key** (the name only): `nexus-config-service-key`

## Live default context

After onboarding, the file at `context_file_path` looks like this. The Orchestrator updates it when a person switches company or product. Work queues live in a `queues/` directory next to it.

```yaml
company: northwind
product: harbor
updated_by: owner@example.com
updated_at: 2026-01-15T12:00:00Z
```
