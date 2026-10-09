# nexa-gauge

[![Built with Ona](https://ona.com/build-with-ona.svg)](https://app.ona.com/#https://github.com/Interested-Deving-1896/nexa-gauge) [![KDE Eco](https://img.shields.io/badge/KDE%20Eco-certified-brightgreen?logo=kde&logoColor=white&style=flat-square)](https://eco.kde.org/) [![Blue Angel](https://img.shields.io/badge/Blue%20Angel-DE--UZ%20215-0055a4?style=flat-square)](https://www.blauer-engel.de/en/certification/criteria)


<!-- AI:start:what-it-does -->
_Description pending._
<!-- AI:end:what-it-does -->

## Architecture

<!-- AI:start:architecture -->
_Architecture documentation pending._
<!-- AI:end:architecture -->

## Install

<!-- Add installation instructions here. This section is yours — the AI will not modify it. -->

```bash
git clone https://github.com/Interested-Deving-1896/nexa-gauge.git
cd nexa-gauge
```

## Usage

<!-- Add usage examples here. This section is yours — the AI will not modify it. -->

## Configuration


For local development or repeatable runs, copy the environment template:

```bash
cp .env.example .env
```

Minimum configuration for OpenAI-backed runs:

```bash
OPENAI_API_KEY=<your-key>
LLM_MODEL=gpt-4o-mini
```

Supported per-node overrides follow this pattern:

```bash
LLM_CLAIMS_MODEL=openai/gpt-4o-mini
LLM_CLAIMS_FALLBACK_MODEL=openai/gpt-4o
LLM_GROUNDING_TEMPERATURE=0.0
LLM_REFALIGN_MODEL=openai/gpt-4o-mini
```

`refalign` uses `EMBEDDING_MODEL` for local semantic similarity. It only uses the configured judge model when a record sets `"refalign": {"atomic_chunks": true}`.

Runtime overrides can also be passed through the CLI:

```bash
nexagauge run eval \
  --input sample.json \
  --llm-model openai/gpt-4o-mini \
  --llm-model grounding=openai/gpt-4o \
  --llm-fallback openai/gpt-4o

# Route all LLM calls through a local or hosted OpenAI-compatible endpoint
nexagauge run eval \
  --input sample.json \
  --host-model-url http://localhost:8080/v1 \
  --llm-concurrency 1 \
  --max-in-flight 1
```

---

## CI

<!-- AI:start:ci -->
_CI documentation pending._
<!-- AI:end:ci -->

## Mirror chain

<!-- AI:start:mirror-chain -->
This repo is maintained in [`Interested-Deving-1896/nexa-gauge`](https://github.com/Interested-Deving-1896/nexa-gauge) and mirrored through:

```
Interested-Deving-1896/nexa-gauge  ──►  OpenOS-Project-OSP/nexa-gauge  ──►  OpenOS-Project-Ecosystem-OOC/nexa-gauge
```

Changes flow downstream automatically via the hourly mirror chain in
[`fork-sync-all`](https://github.com/Interested-Deving-1896/fork-sync-all).
Direct commits to OSP or OOC are detected and opened as PRs back to `Interested-Deving-1896`.
<!-- AI:end:mirror-chain -->

## Contributors

<!-- AI:start:contributors -->
| Contributor | Commits |
|---|---|
| [@Sardhendu](https://github.com/Sardhendu) | 115 |
| [@dependabot[bot]](https://github.com/apps/dependabot) | 1 |
<!-- AI:end:contributors -->

## Origins

<!-- AI:start:origins -->
_Original project — no upstream influences recorded._
<!-- AI:end:origins -->

## Resources

<!-- AI:start:resources -->
_No additional resource files found._
<!-- AI:end:resources -->

## Accessibility

<!-- AI:start:accessibility -->
This repo uses automated accessibility auditing via `check-accessibility.yml`.

Checks include: CODEOWNERS ownership coverage, README screen-reader compatibility,
WCAG 2.1 AA HTML compliance, audio overview (espeak-ng), and Braille output (liblouis).




Run the [Check Accessibility](https://github.com/Interested-Deving-1896/nexa-gauge/actions/workflows/check-accessibility.yml)
workflow to generate the first report and accessibility artifacts.
See the [W3C Web Content Accessibility Guidelines (WCAG)](https://www.w3.org/WAI/standards-guidelines/wcag/)
for the underlying accessibility reference.
<!-- AI:end:accessibility -->

## License

<!-- AI:start:license -->
[MIT](https://github.com/Interested-Deving-1896/nexa-gauge/blob/main/LICENSE) © 2026 [Interested-Deving-1896](https://github.com/Interested-Deving-1896)
<!-- AI:end:license -->
