# Dave-IT-guy

## What is Dave IT Guy?

**Deploy AI stacks with one command.**

Dave IT Guy delivers a **fully containerized** stack with **OpenClaw as its core engine** plus **Ollama** and **Qdrant**, in a single command. No host installs, no config archaeology. Everything runs in Docker; run locally or ship to the cloud. Same stack, anywhere.

### Quick Start (from PyPI)

```bash
pip install dave-it-guy
dave-it-guy deploy openclaw
```

Then open the AI assistant:

```bash
docker exec -it dave-it-guy-openclaw openclaw tui
```

**Gateway:** `http://localhost:18789` · **Qdrant:** `http://localhost:6333/`

### What you get

- **OpenClaw** — AI agent gateway and TUI
- **Ollama** — local LLMs (Llama, Mistral, etc.)
- **Qdrant** — vector memory

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