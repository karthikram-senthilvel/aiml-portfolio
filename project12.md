
# Decision Matrix for Pre-Trained Model Selection

<span class="eyebrow">Project 12 · Model Evaluation & Decision Frameworks</span>

## Overview

An interactive decision matrix comparing four pre-trained models across three domains — NLP/Generative AI, Computer Vision, and Tabular data — on the three axes that actually drive deployment decisions: model size, accuracy, and inference speed.

Rather than presenting a static comparison table, the tool lets you set how much each criterion matters for your use case (via sliders or quick presets like "Edge / On-Device" or "Real-Time Serving") and watches the model ranking re-score live. The goal is to make the trade-off explicit rather than hide it behind a single composite score.

## What's Inside

- **The Trade-Off Triangle** — A visual framing of why no model wins on size, accuracy, and speed simultaneously
- **Four Model Profiles** — GPT-2 (1.5B), BERT-base, EfficientNet-B0, MobileNetV2, and XGBoost, each with sourced size/accuracy/latency figures
- **Live Decision Matrix** — Adjustable priority weights that re-rank all four models in real time, plus four deployment-scenario presets
- **Sourced Footnotes** — Benchmark provenance (GLUE leaderboard, ImageNet, original model papers) and explicit caveats on where figures are task-dependent or not directly comparable

## Key Skills Demonstrated

- Model evaluation and benchmark literacy across NLP, vision, and tabular domains
- Decision framework design — translating qualitative trade-offs into a weighted, interactive scoring tool
- Front-end engineering (HTML/CSS/JS) for data-driven, real-time interactivity
- Technical writing — methodology documentation and sourced analysis (see explanatory document)

## Live Demo

[Open the Decision Matrix →](./assets/model-decision-matrix.html)

## Explanatory Document

The full write-up — introduction, methodology, trade-off analysis, decision matrix, and recommendations by domain — is available as a [Word document](./assets/Model-Selection-Decision-Matrix.docx).
