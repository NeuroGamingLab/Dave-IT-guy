# Dave-IT-guy

## Introducing Dave the MasterClaw

**Deploy AI stacks with one command.**

Dave IT Guy delivers a **fully containerized** stack with **OpenClaw as its core engine** plus **Ollama** and **Qdrant**, in a single command. No host installs, no config archaeology. Everything runs in Docker; run locally or ship to the cloud. Same stack, anywhere.

**From single assistant to self-orchestrating system.**

`dave-it-guy` expands into **dave-the-MasterClaw**: an **agent runtime + orchestrator**. Instead of a single assistant session, you get a system that can **launch goal-driven jobs**, **use tools**, and **fan out** to multiple sub-agents (lightweight workers or full OpenClaw containers) — all without giving the main agent direct Docker control.

![Dave the MasterClaw architecture](docs/dave-the-masterClaw-architecture4-small.png)

### Quick Start (from PyPI)

```bash
pip install dave-it-guy
dave-it-guy deploy openclaw
```

Then open the AI assistant:

```bash
docker exec -it dave-it-guy-openclaw openclaw tui
```

**OpenClaw (gateway):** `http://localhost:18789` · **MasterClaw (API):** `http://localhost:8090` · **Qdrant:** `http://localhost:6333/`

### Run the CLI from Docker (localhost)

Build the image from the source repo, then run with your host Docker socket so `deploy` can start the stack on localhost:

```bash
# From the source repo root
docker build -t dave-it-guy:local .

# Smoke test (no Docker socket needed)
docker run --rm dave-it-guy:local list

# Deploy OpenClaw on localhost
docker run --rm -it \
  -v /var/run/docker.sock:/var/run/docker.sock \
  -v "$HOME/.dave_it_guy:/root/.dave_it_guy" \
  dave-it-guy:local deploy openclaw
```

On Windows (Docker Desktop), use `-v //var/run/docker.sock:/var/run/docker.sock` if needed.

### What you get

- **Agent runtime (OpenClaw)** — tool-using agent gateway + TUI (the “brain” that executes tasks)
- **Orchestrator (MasterClaw)** — a control plane that turns requests into **isolated jobs** and manages lifecycle
- **Multi-agent fan-out** — spin up **lightweight workers** or **full OpenClaw sub-agents** per task (1 : n)
- **Operational UX** — `masterclaw-tui` to create jobs, poll status/results, and clean up sub-agents
- **Shared AI backbone** — **Ollama** (local models / worker backend) + **Qdrant** (shared vector memory)

### Commands

```bash
dave-it-guy list              # Available stacks
dave-it-guy deploy openclaw   # Deploy
dave-it-guy masterclaw-tui    # Launch MasterClaw enhanced terminal UI
dave-it-guy status openclaw   # Status
dave-it-guy logs openclaw     # Logs
dave-it-guy stop openclaw     # Stop stack (preserve data)
dave-it-guy destroy openclaw  # Remove stack
dave-it-guy doctor            # Diagnose issues
dave-it-guy version           # CLI version
```

### Pricing

**Free** — Local stacks. **Pro** — Cloud (Terraform), priority support.

## Links

- **PyPI:** [dave-it-guy](https://pypi.org/project/dave-it-guy/)
- **Project repo:** [NeuroGamingLab/dave-it-guy](https://github.com/NeuroGamingLab/dave-it-guy)
- **Neuro Gaming Lab:** [neurogaminglab.github.io/Neuro-Gaming-Lab](https://neurogaminglab.github.io/Neuro-Gaming-Lab/)

## License

MIT.

---

Built by [NeuroGamingLab](https://github.com/NeuroGamingLab).