# AgentDeck install script

This repository hosts one file: **`install.sh`**, as the only asset of its latest release, so it has a stable link.

```bash
curl -fsSL https://github.com/huru-io/agentdeck-releases/releases/latest/download/install.sh | sh                  # the app + agentdeck, agentdeck-tui
curl -fsSL https://github.com/huru-io/agentdeck-releases/releases/latest/download/install.sh | sh -s -- --server     # … and a server on this computer
curl -fsSL https://github.com/huru-io/agentdeck-releases/releases/latest/download/install.sh | sh -s -- --cli-only   # only agentdeck, agentdeck-tui
```

It runs on a Mac (Apple silicon) or Linux (x86_64; arm64: the CLI and terminal UI), asks nothing, and installs every
file from AgentDeck's public apps package on GitHub's container registry, **`ghcr.io/huru-io/agentdeck-apps`**, checked
against its sha256 first. The server image is **`ghcr.io/huru-io/agentdeck`**. Nothing else is published here.

Already using an AgentDeck server? It serves the same script, set to connect to it: `curl -fsSL https://<your server>/install.sh | sh`,
and its 📦 Get the apps page has the downloads.
