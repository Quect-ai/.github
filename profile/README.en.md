<div align="center">

<img src="./banner.png" alt="Quect — quack a swarm. flat the bill." width="100%">

# 🦆 Quect

### `quack a swarm. flat the bill.`

**Dedicated bandwidth for swarms of coding agents.**
Flat-rate inference: uncapped tokens, dedicated throughput, a predictable bill — no bill-shock.

[Português (BR)](README.md) · **English** · [Español](README.es.md)

[Discord](https://discord.gg/NkY4NzaCfY) · [Waitlist](https://quect.ai) · [quect.ai](https://quect.ai)

> ⚠️ **Pre-launch · June 2026.** Closed beta in waves. Nothing live yet — star + join the waitlist; we'll ping you when the first node is up.

</div>

---

## The problem

The 2026 power-user dev pays **$200–600/mo** in tokens, and the market flipped entirely to metering over the last 12 months. The bill is unpredictable:

- **Copilot** — $29 became **$750**/mo after the metering flip
- **Replit** — $25 plan, surprise **$100–300** bills
- **Uber** — capped engineers at **$1,500/mo** after burning the annual budget in 4 months

Leaving a swarm running 24/7 turns into invoice roulette.

## The fix: broadband for inference

The same leap broadband made over telephony — from per-minute metering → a fixed subscription with dedicated speed. Quect applies it to tokens:

- **🦆 Uncapped tokens** — fixed subscription, loops and swarms 24/7 with no meter running in the background. *(uncapped tokens, fair-use AUP — not "unlimited".)*
- **⚡ Dedicated throughput** — bandwidth in tokens/s per account. Honest, predictable, no fine print.
- **🌊 Queue gateway** — overflow goes into a millisecond queue. Never blocks hard, never bills extra.

## Plug into the tools you already use

**OpenAI-API-compatible** endpoint (+ Anthropic). If your agent/harness speaks the API, point its base URL at Quect — no new CLI, no migration.

```bash
# OpenAI-compatible (Cline, Aider, Codex, Continue, OpenCode…)
export OPENAI_BASE_URL="https://api.quect.ai/v1"
export OPENAI_API_KEY="qk_..."

# Anthropic-compatible (Claude Code)
export ANTHROPIC_BASE_URL="https://api.quect.ai/anthropic"
export ANTHROPIC_API_KEY="qk_..."
```

```bash
curl https://api.quect.ai/v1/chat/completions \
  -H "Authorization: Bearer $OPENAI_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "model": "quect-swarm",
    "messages": [{"role": "user", "content": "refactor this module"}]
  }'
```

*(Endpoints go live per beta wave. The shape above is the target contract.)*

## Multi-model OSS · automatic routing

The right model per task, picked automatically. You never choose the model — the router sends each task to the right one, with fallback, never 429. Frontier (Sonnet/GPT) comes in via pass-through when needed.

| Spec (stealth) | Use case | Lane |
|----------------|----------|------|
| **~12B dense · vision · 256k** | autocomplete · lint-fix · explain · tool-use | fast-lane |
| **~35B MoE · 3B active · 256k** | multi-file refactor · TDD · tool-calling | SWARM driver |
| **~355–600B MoE · ~32B active · 200k** | long-horizon · critical analysis | heavy (pass-through) |

*Catalog curated from the top open-source models on the [LMArena WebDev leaderboard](https://arena.ai/leaderboard/code/webdev?license=open-source) · subject to change.*

## The ladder grows with the swarm

Quect scales node by node. Every waitlist milestone lights up a new node — more dedicated bandwidth, more parallel agents, better models in the curated pool. You never choose or migrate: the router always sends your task to the best model available. More swarm in the community = more muscle for everyone.

## Pricing · pull the bandwidth

No rigid plans. You drag a throughput slider (10 → 150 tok/s) and the price follows, roughly linear: dedicated bandwidth doesn't get cheaper to serve, so there's no hidden volume discount. One pipe, split across as many agents as you want (rule of thumb: ~1 agent per 30 tok/s).

| Throughput | USD/mo | BRL/mo (Pix)¹ |
|-----------|--------|----------------|
| **10 tok/s** | **$0** · free | **R$0** |
| 30 tok/s | $39 | R$199 |
| 60 tok/s | $78 | R$398 |
| 90 tok/s | $117 | R$597 |
| 120 tok/s | $156 | R$796 |
| 150 tok/s | $195 | R$995 |

*Reference points — the slider is continuous on the site, in steps of 10 tok/s. Uncapped tokens, fair-use AUP · tok/s = refill rate; overflow goes into a queue (never-429). ¹ Brazil Pix price — no IOF (3.5% FX tax), local payment. Launch pricing, subject to adjustment.*

> 🦆 **Founding beta: 100 seats.** The first 100 subscribers get a founder badge + seat #1–100, queue priority, and founder & roadmap access. Full price — the perk is status and access, not a discount. Join the waitlist to grab one.

## Get in

1. ⭐ this repo
2. Join the [Discord](https://discord.gg/NkY4NzaCfY)
3. [Waitlist](https://quect.ai) — tell us your current monthly token spend + which harness you use

## License

MIT.

---

<div align="center">
🦆 <i>quack a swarm. flat the bill.</i> · built by <a href="https://quect.ai">Quect.ai</a>
</div>
