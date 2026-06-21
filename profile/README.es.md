<div align="center">

<img src="./banner.png" alt="Quect — quack a swarm. flat the bill." width="100%">

# 🦆 Quect

### `quack a swarm. flat the bill.`

**Ancho de banda dedicado para swarms de agentes de código.**
Inferencia flat-rate: uncapped tokens, throughput dedicado, una factura predecible — sin bill-shock.

[Português (BR)](README.md) · [English](README.en.md) · **Español**

[Discord](https://discord.gg/MuN6VzTEA3) · [Waitlist](https://quect.ai) · [quect.ai](https://quect.ai)

> ⚠️ **Pre-launch · junio 2026.** Beta cerrada por waves. Todavía nada en vivo — dale ⭐ y únete a la waitlist; te avisamos cuando suba el primer nodo.

</div>

---

## El problema

El dev power-user de 2026 paga **$200–600/mes** en tokens, y el mercado entero migró a medición por uso en los últimos 12 meses. La factura es impredecible:

- **Copilot** — $29 se volvió **$750**/mes tras el cambio a metering
- **Replit** — plan de $25, facturas sorpresa de **$100–300**
- **Uber** — limitó a sus ingenieros en **$1.500/mes** tras quemar el presupuesto anual en 4 meses

Dejar un swarm corriendo 24/7 se vuelve una ruleta rusa de factura.

## La solución: banda ancha para inferencia

El mismo salto que la banda ancha dio sobre la telefonía — de pagar por minuto → una suscripción fija con velocidad dedicada. Quect lo aplica a los tokens:

- **🦆 Tokens sin tope** — suscripción fija, loops y swarms 24/7 sin medidor corriendo de fondo. *(uncapped tokens, fair-use AUP — no "unlimited".)*
- **⚡ Throughput dedicado** — ancho de banda en tokens/s por cuenta. Honesto, predecible, sin letra chica.
- **🌊 Queue gateway** — el exceso entra en una cola de milisegundos. Nunca bloquea, nunca cobra de más.

## Conéctalo a las herramientas que ya usas

Endpoint **compatible con la API de OpenAI** (+ Anthropic). Si tu agent/harness habla la API, apunta su base URL a Quect — sin CLI nuevo, sin migración.

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
    "messages": [{"role": "user", "content": "refactoriza este módulo"}]
  }'
```

*(Los endpoints entran en vivo por wave de beta. El contrato de arriba es el objetivo.)*

## Multi-modelo OSS · routing automático

El modelo correcto para cada tarea, elegido automáticamente. Nunca eliges el modelo — el router manda cada tarea al modelo indicado, con fallback, nunca 429. Frontier (Sonnet/GPT) entra por pass-through cuando se necesita.

| Spec (stealth) | Caso de uso | Lane |
|----------------|-------------|------|
| **~12B dense · vision · 256k** | autocomplete · lint-fix · explain · tool-use | fast-lane |
| **~80B MoE · 3B active · 256k** | refactor multi-file · TDD · tool-calling | SWARM driver |
| **~355–600B MoE · ~32B active · 200k** | long-horizon · análisis crítico | heavy (pass-through) |

*Catálogo curado entre los mejores modelos open-source del [LMArena WebDev leaderboard](https://arena.ai/leaderboard/code/webdev?license=open-source) · sujeto a cambios.*

## Planes

| Tier | USD/mes | BRL/mes (Pix)¹ | Throughput | Agentes |
|------|---------|----------------|------------|---------|
| **FREE** | $0 | R$0 | 15 tok/s | 1 |
| **BASE** | $39 | R$199 | 30 tok/s | 1 |
| **PRO** | $76 | R$399 | 60 tok/s | 2 |
| **SWARM** ⭐ | $150 | R$790 | 90 tok/s | 3 |
| **MAX** | $284 | R$1.490 | 120 tok/s | 4 |

*Uncapped tokens, fair-use AUP · tok/s = tasa de recarga; el exceso entra en cola (never-429). ¹ Precio BR vía Pix — sin IOF (3,5% impuesto FX), pago local. Planes sujetos a ajuste hasta el launch.*

> 🦆 **Beta founding: 100 plazas al 50% off.** Los primeros 100 suscriptores fijan la mitad del precio mientras mantengan la suscripción. Entra a la waitlist para conseguir la tuya.

## Únete

1. ⭐ este repo
2. Únete al [Discord](https://discord.gg/MuN6VzTEA3)
3. [Waitlist](https://quect.ai) — cuéntanos cuánto gastas/mes en tokens + qué harness usas

## Licencia

MIT.

---

<div align="center">
🦆 <i>quack a swarm. flat the bill.</i> · hecho por <a href="https://quect.ai">Quect.ai</a>
</div>
