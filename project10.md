# Explainable AI — Inside the Black Box

This artifact is an interactive visual infographic explaining Explainable AI (XAI): why transparency in AI is critical, why it is technically hard, how explanations and models are validated, and what techniques industry leaders use to make modern AI understandable.

[**▶ View the live infographic**](./assets/explainable-ai-infographic.html)

## Objective

To research and communicate how the AI field is working to make models like GPT, Claude, Gemini, and LLaMA understandable and accountable — and to demonstrate a different skill set from my first portfolio artifact by building the piece as a self-contained, deployable web product rather than a slide deck.

## Process

To create this artifact, I followed these steps:

1. Researched current explainability work, grounding the content in recent developments — Anthropic's open-sourced circuit-tracing tools, Google DeepMind's Gemma Scope sparse autoencoders, the SAE faithfulness debate, and the EU AI Act compliance timeline.
2. Organized the findings into four themes: what XAI is and why it matters; the challenges (model scale, polysemanticity, opaque reasoning, regulatory pressure); validation and performance metrics; and current solutions and techniques.
3. Designed and built an interactive HTML infographic around a single "opening the black box" metaphor, with a two-tier metrics breakdown and technique cards grouped by approach (post-hoc attribution vs. mechanistic interpretability).
4. Performed visual QA across all sections and deployed the file to GitHub Pages as a live, shareable web page.

## Key Concepts Covered

- **Explainable AI & its importance** — interpretability vs. explainability, and the gap between an *accurate* model and an *accountable* one.
- **Challenges in explainability** — model complexity, distributed/superimposed features, the risk that stated reasoning is not true reasoning, and regulatory requirements (EU AI Act, GDPR, NIST AI RMF).
- **Validation & performance metrics** — faithfulness, robustness, completeness, and comprehensibility for explanations; accuracy/F1/AUC, calibration, drift robustness, and hallucination rate for models.
- **Current solutions & techniques** — SHAP, LIME, Integrated Gradients, DeepLIFT, attention/saliency; sparse autoencoders, circuit tracing and attribution graphs, and reasoning transparency.

## Skills Demonstrated

Applied AI research synthesis, technical communication, front-end / data-visualization design, and web deployment via GitHub Pages.
