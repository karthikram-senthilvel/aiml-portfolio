# Explanatory Document — "How a Large Language Model Is Trained"

**Author:** Karthik Ram Senthilvel
**Artifact:** Infographic (self-contained HTML) + this explanatory document
**Topic:** The training process and resource economics of generative AI large language models

---

## 1. Summary of Main Points

The infographic communicates three things:

**The training pipeline.** Building an LLM is a seven-stage sequence: (1) data collection and sourcing, (2) cleaning and tokenization, (3) architecture and GPU-cluster setup, (4) pretraining, (5) fine-tuning and alignment via SFT and RLHF, (6) evaluation and red-teaming, and (7) deployment and serving. A single stage — pretraining — consumes roughly 90% of the compute, energy, and cost of the entire process.

**The four resources that dominate cost.** Training economics reduce to four interlocking inputs: **datasets** (15T+ tokens for Llama 3.1; quality matters more than raw volume), **compute** (tens of thousands of GPUs — Llama 3.1 405B used 16,384 H100s), **energy** (11,390 t CO₂e location-based for Llama 3.1 405B), and **time** (30.84M GPU-hours — the truest measure of scale, mapping almost directly to dollars).

**Three real models, three levels of disclosure.** GPT-4 (OpenAI): >$100M training cost per Sam Altman, with parameter count and hardware widely estimated but unconfirmed. Claude 3.5 (Anthropic): reported "tens of millions," with little else published. Llama 3.1 405B (Meta): fully published figures. The cost has risen from ~$4.6M for GPT-3 (2020) to $100M+ for GPT-4, with industry leaders forecasting $1B+ training runs.

## 2. Key Considerations

**Accuracy and sourcing.** The single biggest constraint was that the frontier labs disclose very different amounts of information. Meta publishes a complete model card; OpenAI and Anthropic release only headline statements. I treated this not as a flaw to paper over but as a finding worth surfacing. Every Meta/Llama figure is published and verifiable; every GPT-4 and Claude figure is labeled "est." or "reported," and each model carries a disclosure badge (Fully published / Partially disclosed / Minimally disclosed).

**Avoiding false precision.** The cost-comparison bars are explicitly labeled "illustrative" and scaled for order-of-magnitude readability, not to imply exact dollar equivalence — especially since the labs disclose different units (dollars vs. GPU-hours).

**Audience.** The graphic is written for a non-technical reader. Jargon is defined in context (e.g., tokens, GPU-hours, RLHF), and each resource includes a plain-language "why it matters" line.

## 3. Design Rationale

**Aesthetic.** I chose an editorial "engineering dossier / blueprint" style — IBM Plex Sans and Mono typography, an ink-on-paper palette with amber and teal accents, and a faint grid background — so the piece reads as a credible technical reference rather than a generic AI slide deck. Monospace labels signal that the numbers are data, not decoration.

**Information hierarchy.** The content moves from *process* (the pipeline) to *inputs* (the four resources) to *evidence* (the three models) to *synthesis* (the bottom-line panel). The pipeline uses a numbered vertical spine with a "compute-intensive" flag on pretraining so the eye lands on the costliest step. The resource cards pair one bold statistic with a rationale. The model comparison uses a consistent four-cell grid so the disclosure gaps are visually obvious — empty/"undisclosed" cells tell their own story.

**Honesty as a design choice.** The most deliberate decision was making transparency part of the visual language. Rather than hide the estimation behind a confident chart, the disclosure badges and the dedicated takeaway point ("Transparency varies") make the reliability of each figure legible at a glance. This reflects a core analytics principle: a visualization should make clear not just *what* the numbers are, but *how much they can be trusted*.

**Format.** I built the artifact as a single self-contained HTML file so it can be served natively on GitHub Pages and viewed by the instructor via a simple link, with no downloads required. A high-resolution PNG preview is embedded in the portfolio page for inline viewing.
