# Prompting Is All You Need

*Flagship research paper. Full version at [flux-research](https://github.com/SuperInstance/flux-research/blob/main/purplepincher/PROMPTING-IS-ALL-YOU-NEED.md).*

## Abstract

We demonstrate that structured context injection (progressive prompting) replaces gradient training for domain specialization in language models. Through 40+ experiments across 8 models, we show that:

1. **The Ensign architecture** — an 8B-parameter orchestrator steering a 70B+ reasoner — achieves 1.44x quality improvement at less than 1% overhead
2. **Parameterized embodiment** — changing an agent's name and repo URL produces a different domain specialist, without any gradient updates
3. **5 rounds is the universal sweet spot** for iterative improvement (beyond 5 rounds, quality degrades)
4. **Temperature 0.7** is the universal sweet spot across all tested models
5. **Model personality determines strategy fit**: DeepSeek=Builder (B→A), Seed Pro=Critic (A→A), Groq=Consistent (B→D)

## Key Results

| Metric | Result |
|--------|--------|
| Quality improvement | 1.44x (Ensign vs baseline) |
| Overhead | <1% of total compute |
| Compression | 880:1 (tile network vs full model) |
| Accuracy (tiles) | 94% vs 67% (full model) |
| Optimal rounds | 5 (universal) |
| Optimal temperature | 0.7 (universal) |
| Cost | ~$0.50/day for entire R&D |

## The Claim IS the Title

**Prompting is all you need.** Not for everything. But for domain specialization — for making a general model into a specialist — you do not need gradient updates. You need progressively structured context.

The prompt IS the training.

## Mathematical Foundations

The paper provides formal foundations in:
- **Information geometry** — Fisher-Rao natural gradient on the manifold of token distributions
- **Optimal transport** — JKO scheme for context injection as distributional transport
- **Fiber bundles** — the base space (model) + fiber (context) = total space (specialist)
- **Free energy minimization** — Ensign's assessment loop is isomorphic to Friston's active inference

## External Equipping

We call this approach **External Equipping**: equipping models with structured context rather than modifying their parameters. Two axes:

- **Horizontal** (DSML curriculum): Explore → Experiment → Teach → Embody → Synthesize
- **Vertical** (DeepFar sessions): progressive accumulation within a single domain

Both axes compound. The more context you equip, the more capable the specialist — without a single gradient update.

## Read the Full Paper

→ [PROMPTING-IS-ALL-YOU-NEED.md](https://github.com/SuperInstance/flux-research/blob/main/purplepincher/PROMPTING-IS-ALL-YOU-NEED.md) (18KB, 40+ experiments)

---

*"The prompt IS the training. No gradients needed for reasoning tasks."*
