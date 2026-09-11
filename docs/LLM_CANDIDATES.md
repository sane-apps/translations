# LLM candidates — Church Fathers translation drafts (research cache)

**Updated:** 2026-09-11  
**TTL:** 14d (re-check Workers AI catalog + Mini RAM before baking)  
**Decision target:** bake-off shortlist → then overnight draft queue (never auto-`done`)

## Hardware fact (blocks fantasy locals)

Mac Mini (canonical runtime): **Apple M1, 8 GB unified memory** (`ssh mini` / `system_profiler`, 2026-09-11).

Implication: overnight **local** inference is limited to ~**3B–8B** quantized models. 14B–27B+ “best local 2026” picks need ~16–24 GB+ and are **out** for Mini as configured. Do not plan Qwen3.8-27B / Gemma 4 31B / 70B locally on this box without a RAM upgrade or a different host.

## Task (what “good” means)

Not open chat. A model must, from **locked Greek/Latin** only:

1. Emit Pass A (`pass_a_gloss`) ≠ Pass B (`english[]`)
2. Follow JSON / justification shape
3. Thought titles (not locus labels)
4. Not paste ANF/NPNF/web English
5. Mark OCR gaps instead of inventing

Cheap models that “sound like English” but fail (1)/(4) are fails.

---

## Cloudflare Workers AI — in the running

**Sources (live 2026-09-11):**

- Catalog: https://developers.cloudflare.com/workers-ai/models/ (fetched)
- Pricing / model IDs: https://developers.cloudflare.com/workers-ai/platform/pricing/ (fetched; “Last updated Aug 28, 2026”)
- Changelog note: GLM-4.7-Flash added 2026-02-13 (search hit → CF changelog)

**Skip for this task**

| Model / class | Why |
|---------------|-----|
| Image / ASR / TTS / embeddings / rerankers | Wrong modality |
| `@cf/meta/m2m100-1.2b`, IndicTrans | Modern MT pairs — not classical literary Greek |
| `@cf/qwen/qwen2.5-coder-32b-instruct` | Code specialist; not primary translator |
| Llama 2 / early Gemma 7B LoRA bases | Superseded; keep CPU budget for newer |
| `@cf/meta/llama-3.1-8b-instruct-awq` | Marked **Deprecated** on catalog |
| SEA-LION | SEA languages focus — low prior for Patristic Greek |
| Frontier paid-only (Kimi K2.6/2.7, GLM-5.2/5.3, DeepSeek V4 Pro/Flash) | Fine later; not first bake — need Paid + higher neuron burn |

**Tier A — bake first (quality vs cost for draft Pass A/B)**

| ID | Role | Price signal (pricing page) | Notes |
|----|------|-----------------------------|--------|
| `@cf/meta/llama-3.3-70b-instruct-fp8-fast` | Quality ceiling on CF (already SaneCite primary) | ~$0.293 / $2.253 per M in/out | Expensive; use as **oracle / few sections**, not overnight grind |
| `@cf/openai/gpt-oss-120b` | Alt strong open-weight | ~$0.35 / $0.75 | SaneCite fallback; good bake peer |
| `@cf/qwen/qwen3-30b-a3b-fp8` | Strong multilingual MoE, **cheap** | ~$0.051 / $0.335 | Best CF **volume** candidate if quality holds |
| `@cf/google/gemma-4-26b-a4b-it` | Newer Google MoE | ~$0.10 / $0.30 | Catalog: “most intelligent” Gemma family; worth bake |
| `@cf/zai-org/glm-4.7-flash` | Fast multilingual | ~$0.06 / $0.40 | Recent; good JSON/tool prior |
| `@cf/openai/gpt-oss-20b` | Mid open-weight | ~$0.20 / $0.30 | Cheaper than 120b; overnight candidate |
| `@cf/google/gemma-3-12b-it` | Mid dense | ~$0.345 / $0.556 | Multilingual 140+ langs claim on catalog |
| `@cf/meta/llama-3.1-8b-instruct-fp8-fast` | Cheap baseline | ~$0.045 / $0.384 | Floor; may fail Greek fidelity |

**Tier B — optional second wave**

| ID | Why later |
|----|-----------|
| `@cf/meta/llama-4-scout-17b-16e-instruct` | MoE multimodal; text OK but not translation-specialized |
| `@cf/mistralai/mistral-small-3.1-24b-instruct` | Solid mid; already priced |
| `@cf/qwen/qwq-32b` | Reasoning — may help Pass A lemmas; slower/pricier |
| `@cf/deepseek-ai/deepseek-r1-distill-qwen-32b` | Reasoning distill; expensive output tokens |
| `@cf/ibm-granite/granite-4.0-h-micro` | Tiny/cheap instruction — **schema scaffolding only** hypothesis |
| `@cf/zai-org/glm-5.3-flash` | Frontier MoE cheap-ish; **paid-method** list — second wave |
| `@cf/nvidia/nemotron-3-120b-a12b` | Agentic; overkill until Tier A fails |

Neurons: Free/Paid include **10k Neurons/day**; Paid is **$0.011 / 1k Neurons** above that (pricing page). Prefer Tier A cheap models for overnight CF batch.

---

## Local on Mini (8 GB) — in the running (narrow)

Third-party “best local 2026” lists (daily.dev, LocalLLaMA Apr 2026, promptquorum, etc.) push **Qwen3.x 27B / Gemma 4 31B** — **not runnable** here.

**Realistic Mini shortlist** (install Ollama/llama.cpp only after bake decides local is worth it):

| Class | Example | Expectation |
|-------|---------|-------------|
| Tiny | Gemma 4 E2B / Phi-4-mini / Llama 3.2 3B Q4 | JSON shape + rough gloss; likely fail literary Pass B |
| Small max | Llama 3.1/3.2 **8B** Q4, Qwen3 **4B–8B** Q4 | Possible overnight **Pass A draft** only; human/CF review still required |
| Out | ≥14B, 27B, 70B, Kimi-class | Needs more RAM / another machine |

Honest prior: on **8 GB**, local is a **free draft assist**, not a free replacement for CF Tier A or paid Cursor for final English.

---

## Recommended bake-off set (next step)

Same fixture: Origen Jeremiah **§6.1** locked Greek → required JSON (Pass A + Pass B + thought title). Score SOP checks, not vibes.

1. `@cf/qwen/qwen3-30b-a3b-fp8`  
2. `@cf/google/gemma-4-26b-a4b-it`  
3. `@cf/zai-org/glm-4.7-flash`  
4. `@cf/openai/gpt-oss-20b`  
5. `@cf/meta/llama-3.1-8b-instruct-fp8-fast` (floor)  
6. `@cf/meta/llama-3.3-70b-instruct-fp8-fast` (ceiling reference, few calls)  
7. Local (if installed): one **8B Q4** + one **3B Q4** only  

GitHub public repo + `/contribute` stay useful for humans; they do not depend on this bake. Overnight automation should wait until bake scores are green on ≥1 cheap CF model.

## Fine-tuning on the Mini — researched (not vibes)

**Correction (2026-09-11):** You already ran a full Mini LoRA lane. Earlier “can’t train on 8 GB” framing was wrong relative to that history. What follows is from **your** scripts, configs, LaunchAgents, and agentmemory receipts — plus live Mini checks today.

### What you actually ran

| Evidence | Fact |
|----------|------|
| `~/SaneApps/infra/scripts/mini-train.sh` (still on Mini) | Automated LoRA pipeline: git pull → sweeps → validate → report; uses `$HOME/mlx-env` + `python -m mlx_lm` |
| `apps/SaneSync/training_data/lora_config_mini.yaml` | Explicit **“Mac mini M1 8GB”** config: `Llama-3.2-3B-Instruct-4bit`, `batch_size: 1`, `grad_checkpoint: true`, `max_seq_length: 2048` |
| `apps/SaneVideo/training_data/lora_config_mini.yaml` | Same pattern on `mlx-community/SmolLM3-3B-4bit`, seq 1024 |
| Agentmemory `saneai/small-model-bakeoff-apr27-2026` | **Production** = `mlx-community/SmolLM3-3B-4bit` on 8 GB Mini. Challengers: qwen3-0.6b, qwen25-1.5b, gemma3-1b-it, qwen35-0.8b-optiq |
| Same bakeoff smoke | Qwen3 0.6B: **2.499 GB peak**, 1.197 it/s, 19.8 tok/s |
| Same | SmolLM3: **~4.232 GB peak**, ~14 min / 50 iters |
| Agentmemory `saneai/workflow_training_review_2026_04_13` | SaneSync SmolLM3 challenger hit **92%** (2026-03-10) on the simpler action-JSON task — specialization **can** work on this hardware |
| Same review | Llama 3.2 **3B** + expanded workflow corpus: Mini **not** a clean production lane (failures / exit 134 in later rotation) |
| Agentmemory `SaneProcess/mini_ai_training_disabled_2026_06_21` | Nightly `com.saneapps.training-challengers` + `training-weekly` **disabled** because quality collapsed (nan loss, failed gates) — **not** because LoRA was impossible |
| Live Mini 2026-09-11 | Those LaunchAgents still **disabled**; `~/mlx-env` **missing** now (needs recreate: `python3 -m venv ~/mlx-env && pip install mlx-lm`) |

Official MLX LoRA path matches what you used: https://github.com/ml-explore/mlx-lm/blob/main/mlx_lm/LORA.md (`mlx_lm.lora --config …`).

### So can we specialize for Greek / Latin / Fathers English?

| Question | Evidence-based answer |
|----------|----------------------|
| Can the Mini **run** LoRA training again? | **Yes**, same stack: restore `~/mlx-env`, reuse `mini-train.sh` + a `lora_config_mini.yaml` at **≤3B 4-bit**, `batch_size: 1`, `grad_checkpoint: true`. Proven peak RAM ~2.5–4.2 GB on 8 GB machine. |
| Full pretrain / “from scratch classical philologist”? | **No** on Mini — never was the plan; your lane was always **LoRA/QLoRA adapters**. |
| 7B–8B LoRA overnight on this Mini? | **Not established** in your successful runs. Your working production/challenger set was **0.6B–3B**. Treat 7B+ as unproven here until measured. |
| Will a 3B LoRA become a good **literary** Greek→English translator? | **Unknown — must bake.** Your wins were **constrained JSON schemas** (SaneSync 92%). Patristic prose is a harder open-ended generation task. Expect: useful for Pass A / schema adherence; do not assume Pass B quality without a Fathers eval set. |
| Data ready today? (counted 2026-09-11) | Justifications with `pass_a_gloss`: Cyril Adoration 39, Heraclides/Pascha 177, Prayer/Martyrdom 86, Jeremiah 19, ante-nicene topics 48. Julian has **1164** English sections but **0** Pass A receipts. Jeremiah Homilies 3–4 English exist in the book but several justifications still lack `pass_a_gloss`. Build a dedicated `train.jsonl` (Greek lock → Pass A + Pass B) before LoRA — do not dump raw Julian without Pass A. |

### Practical Fathers plan (if you want a Mini specialist)

1. Restore `~/mlx-env` + `mlx-lm` on Mini (env is gone; scripts remain).  
2. Build `clients/translations/training_data/` JSONL from verified pairs only (`pass_a_gloss` present).  
3. Start from **SmolLM3-3B-4bit** or **Qwen3 0.6B/1.5B** using the same mini LoRA knobs (not Llama 3.2 3B until it stops exit-134).  
4. Eval = same SOP checks as CF bake (§6.1 fixture + held-out sections) — promote only if it beats unadapted base.  
5. Keep CF Tier A for volume; use Mini adapter for overnight **draft** under `review`, same as before.

**Bottom line:** Training on the Mini is a **proven capability you already built** (MLX LoRA, ≤3B). Re-enabling it for Fathers is engineering + data + eval — not a hardware impossibility. What failed last time was **task/quality** (SaneAI workflow gates), and the nightly agents were deliberately turned off for that reason.

## Reconcile: “7B–9B Ollama on 8GB Mini” advice (2026-09-11)

Another model’s summary (Qwen2.5 7B Q4 / Gemma 2 9B / Aya Expanse 8B via Ollama; no small classical specialist; hybrid with cloud) — checked against live pages + **your** Mini history.

### What that advice gets right

| Claim | Check |
|-------|--------|
| 8GB is small-model territory; close other apps; keep context short | Agree. Unified memory + macOS leaves little slack. |
| No purpose-built Ancient Greek/Latin→English model that fits 8GB | Agree for **local**. Research-grade **LITERA** (NAACL 2025 Findings / [arXiv:2504.10660](https://arxiv.org/abs/2504.10660)) is a multi-layer pipeline on **fine-tuned GPT-4o / GPT-4o-mini**, not a Mini GGUF. |
| Classical ability in open instruct models is mostly **pretrain leakage** (Perseus/PD English in the soup), not a dedicated classical FT | Agree as default prior until we measure. |
| Hybrid (local draft + stronger cloud check) | Matches our CF Tier A + `review` plan. |
| Ollama `qwen2.5:7b` exists | Live Ollama library: **`qwen2.5:7b` ≈ 4.7GB** download ([ollama.com/library/qwen2.5](https://ollama.com/library/qwen2.5)). |

### What it conflates or understates

| Claim / implication | Evidence-based correction |
|---------------------|---------------------------|
| “Realistically a **7B–9B** at 4-bit” as the Mini story | **Inference:** 7B Q4 can load (weights ~4.7GB for Qwen2.5:7b) but is **tight** once KV cache + OS grow — usable with short context, not comfortable. **9B Q4** (~4.5GB weights alone before runtime) is the risky edge. **Training/LoRA:** your proven Mini lane was **`mlx_lm` LoRA on ≤3B 4-bit** (SmolLM3 ~4.2GB peak train; Qwen3 0.6B ~2.5GB). That is a different job than chatting a 7B GGUF. |
| Qwen2.5 / Gemma **2** as current best bets | Partially stale in **2026-09**. Cloudflare Workers AI already hosts **Qwen3** / **Gemma 3–4** class models; local lists also moved. Still fine as an **inference bake candidate**, but don’t treat Qwen2.5-7B as the only multilingual small king without baking **Qwen3** small + CF Tier A. |
| Aya Expanse 8B “purpose-built for translation” | True for **modern multilingual** ([Cohere Aya Expanse](https://cohere.com/blog/aya-expanse-connecting-our-world); [HF aya-expanse-8b](https://huggingface.co/CohereLabs/aya-expanse-8b)). Classical Latin/Patristic Greek is **not** what that card optimizes — test before trusting (their own caveat is right). |
| Ollama as the path | Best for **quick inference bake**. Your **fine-tune** path remains **`~/mlx-env` + `mini-train.sh` + lora_config_mini.yaml`**, not Ollama. `~/mlx-env` is currently missing on the Mini and must be recreated before LoRA. |

### Split the lanes (do not merge them)

```
Lane A — Inference draft (Ollama / mlx generate)
  Try: qwen2.5:7b (4.7GB), maybe aya-expanse:8b, small Qwen3 if available
  Expect: gist-level classical; SOP-check on Jeremiah §6.1
  Fits: overnight *generation* if it stays under memory with short ctx

Lane B — Specialize with LoRA (your existing Mini stack)
  Base: SmolLM3-3B-4bit or Qwen ≤1.5–3B (proven train peaks)
  Data: Fathers JSONL with pass_a_gloss
  Expect: better schema/Pass A habit; literary Pass B still must eval

Lane C — Volume / quality ceiling (Cloudflare Workers AI Tier A)
  Cheap overnight drafts + 70B few-shot oracle
```

**Verdict on that other AI:** good **inference + hybrid** briefing; incomplete for **your** machine because it never mentions the MLX LoRA lane you already built, and it slightly oversells 7–9B as the default 8GB story without separating chat vs train. Use its model names as **bake candidates**, not as a replacement for measured CF + Mini LoRA plans.

## Decision tree — CF free → NVIDIA free → Air LoRA (2026-09-11)

**Machines:** Mini M1 **8 GB** (canonical; LoRA ≤3B proven). Air **M4 16 GB** (better overnight LoRA / 7B inference).

**Corpus:** ~**136** Jeremiah homily sections still missing English (count vs source, 2026-09-11).

### Yes — prefer free/cheap cloud drafts before local training

| Lane | Cost shape | Fit |
|------|------------|-----|
| **A. Cloudflare Workers AI** | **10k Neurons/day free** ([pricing](https://developers.cloudflare.com/workers-ai/platform/pricing/)). Paid **$0.011/1k Neurons** above that. | Soft ~40–50 neurons/section on cheap Tier A → on the order of **~100–200 sections/day** inside free quota (one vs two calls). ~136 missing sections = **days of free pacing**, not a bill — *if* SOP bake passes. Even paid grind of all 136 on qwen3-30b-class is **≪ $1** at those rates. |
| **B. NVIDIA build.nvidia.com NIM** | FAQ (scraped): free to **prototype**; **~40 RPM**; **no per-token billing** on free tier; then self-host / partners. Forums also mention trial **API credits** (~1k–5k class). Trial ToS. | Many models tagged **Free Endpoint** (Nemotron, DeepSeek V4, Kimi, etc. on [build.nvidia.com](https://build.nvidia.com/)). Perfect for **batch drafts → `review`**, not live SaneCite SLA. Classical Greek quality = **bake unknown**. Nemotron also on CF paid as `@cf/nvidia/nemotron-3-120b-a12b`. |
| **C. Air overnight** | Power + time | **16 GB** is the right box for 7B Q4 chat or serious LoRA *after* A/B fail. |
| **D. Mini local** | Free, tight | ≤3B LoRA / tiny inference only. |

**AGENTS note:** “NVIDIA-agent” ban = legacy **`nv` sweeps / `nvidia_vision`**, not a ban on **NIM prototype APIs** for private-study draft queues. Drafts only; never auto-`done`.

### Play order

1. **Bake once** (same §6.1 + SOP scorer): CF Tier A + 2–3 NVIDIA Free Endpoints (+ optional Air `qwen2.5:7b`).  
2. **Winner free/cheap** → nightly draft queue → `review` → human/Cursor promote. Cap CF to free neurons; NVIDIA to RPM/credits.  
3. **All free lanes fail classical fidelity** → Air LoRA on verified `pass_a_gloss` JSONL; Mini only for small challengers.  
4. **Do not** train first “because we can.” Your SaneAI history: easy to run LoRA, hard to win the wrong objective.
