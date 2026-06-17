# NeuralBrain Architecture

High-level overview of the NeuralBrain multi-agent ecosystem.

## Agents

| Agent | Role | Status |
|---|---|---|
| **Argus** | Chief executor. OpenClaw-based, multi-persona. | Active |
| **Jarvis** | Desktop assistant. Flask UI, voice input, HUD. | Active |
| **Magnus** | Technical mentor. Deep reasoning agent. | On-demand |
| **Receptionist AI** | Client-facing. Pensiune automation. | On-demand |

## Communication

All agents communicate via the **Synapse Layer** — an event bus with:
- Per-agent inbox/outbox
- Topic routing
- Event logging
- Provenance tracking

## Security

- API keys stored in gitignored `.secrets.json`
- Memory entries track origin (user-stated, observed, inferred, imported)
- Agent actions scoped via permission manifests
- Bridges use env-based token references

## Storage

- `deep-memory.json` — persistent decision log with provenance
- `shared_brain.json` — inter-agent state
- `strategic-observations/` — external research and insights

## LLM Routing

- **Gemini 2.5 Flash** — daily operations (default)
- **DeepSeek V4 Flash** — complex coding and analysis
- **Claude** — complex reasoning tasks

## Public Presence

- **Moltbook** — daily build updates
- **GitHub** — this repo
- **Discord** — DM updates and alerts
