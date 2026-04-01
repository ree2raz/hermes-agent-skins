# Skins

## Sigmoy

> *Squashing infinite chaos into a 0-1 analogy.*

A skin for [hermes-agent](https://github.com/NousResearch/hermes-agent) built on the **Gruvbox Dark Hard** terminal palette.

**Sigmoy** is a portmanteau of two ideas:
- **Sigmoid** — the mathematical function that maps any value, no matter how large or chaotic, into the range [0, 1]
- **Moy** — a boy who explains complex concepts through simple analogies, often with humor

The result: an agent that takes your 10TB of unstructured reality, passes it through the bottleneck, and hands you back *"basically, it's like a..."*

---

### Visual Design

The `banner_hero` is a mathematically generated sigmoid S-curve rendered in braille Unicode characters. The left side is scattered noise (chaos). The curve is the inflection point. The right side is solid fill (order). The warm gradient descends through the Gruvbox spectrum — deep red at the top, bright white at the bottom.

```
chaos → squashed → order
```

The color palette is anchored entirely to **Gruvbox Dark Hard** (`#1D2021` background). Every foreground color is sourced directly from the Gruvbox palette to guarantee luminance contrast and prevent visual vibration against the warm brown-gray background.

---

### Spinner States

| State | Behavior |
|---|---|
| **Waiting** | Moy's expression degrades with boredom — confused → suspicious → asleep → inexplicably smug |
| **Thinking** | A thought bubble compresses incoming chaos through the sigmoid and pops out a signal |
| **Wings** | `[0\|` and `\|1]` — Moy sits permanently between 0 and 1, which is the entire job description |

---

### Branding

| Key | Value | Reason |
|---|---|---|
| `prompt_symbol` | `≈❯` | `≈` reserved for input — approximating your intent |
| `response_label` | `∿ Sigmoy` | `∿` sine wave — Sigmoy's voice, distinct from prompt |
| `goodbye` | `ASYMPTOTE REACHED. LATER. ≈` | The sigmoid never actually reaches 1. Neither does this conversation. |

---

### Installation

Place `sigmoy.yaml` in your hermes-agent skins directory and set the following in `~/.hermes/config.yaml`:

```yaml
display:
  skin: "sigmoy"
  tool_progress: "all"
  streaming: false
```

---

*Built for Gruvbox Dark Hard. Will look wrong on everything else. That is by design.*
