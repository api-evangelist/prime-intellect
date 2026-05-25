# Prime Intellect

Prime Intellect is an open, decentralized stack for developing and improving AI agents through reinforcement learning. This API Evangelist catalog entry profiles the company's full developer surface: GPU compute marketplace, hosted RL post-training ("Lab"), secure remote sandboxes, OpenAI-compatible inference, evaluations against the Environments Hub, and account/team platform APIs.

## Provider

- Website: https://www.primeintellect.ai
- Docs: https://docs.primeintellect.ai
- App / Dashboard: https://app.primeintellect.ai
- API Reference: https://docs.primeintellect.ai/api-reference/introduction
- OpenAPI: https://api.primeintellect.ai/openapi.json
- GitHub org: https://github.com/PrimeIntellect-ai

## APIs

| API | Base URL | OpenAPI |
|---|---|---|
| Prime Intellect Compute API | https://api.primeintellect.ai | [openapi/prime-intellect-compute-api-openapi.yml](openapi/prime-intellect-compute-api-openapi.yml) |
| Prime Intellect Sandbox API | https://api.primeintellect.ai | [openapi/prime-intellect-sandbox-api-openapi.yml](openapi/prime-intellect-sandbox-api-openapi.yml) |
| Prime Intellect Training API | https://api.primeintellect.ai | [openapi/prime-intellect-training-api-openapi.yml](openapi/prime-intellect-training-api-openapi.yml) |
| Prime Intellect Evaluations API | https://api.primeintellect.ai | [openapi/prime-intellect-evaluations-api-openapi.yml](openapi/prime-intellect-evaluations-api-openapi.yml) |
| Prime Intellect Inference API | https://api.pinference.ai/api/v1 | [openapi/prime-intellect-inference-api-openapi.yml](openapi/prime-intellect-inference-api-openapi.yml) |
| Prime Intellect Platform API | https://api.primeintellect.ai | [openapi/prime-intellect-platform-api-openapi.yml](openapi/prime-intellect-platform-api-openapi.yml) |

All control-plane surfaces share the same bearer-token API key (`Authorization: Bearer $PRIME_API_KEY`). The inference plane runs on a separate hostname (`api.pinference.ai`) and uses the same key.

## Artifacts

- `apis.yml` — APIs.json index for this provider
- `openapi/` — six OpenAPI 3.1 specs split by product surface, derived from the upstream `api.primeintellect.ai/openapi.json` (Compute, Sandbox, Training, Evaluations, Platform) plus an authored Inference spec for `api.pinference.ai`
- `capabilities/` — Naftiko 1.0.0-alpha2 capabilities (one per business surface) with REST and MCP adapters
- `json-schema/` — Core entity schemas (Pod, Sandbox, Training Run, Evaluation)
- `json-ld/` — Linked-data context covering Pod, Sandbox, TrainingRun, Evaluation, Disk, Wallet, Usage
- `plans/` — API Commons Plans 0.1 for compute, training, and inference pricing
- `rate-limits/` — API Commons Rate Limits 0.1 (best-effort; not all limits are publicly documented)
- `finops/` — FOCUS-aligned FinOps definition spanning GPU-hours and token meters

## CLI and SDK

- `pip install prime` — official CLI + Python SDK (`prime pods`, `prime sandbox`, `prime env`, `prime train`, `prime eval`, `prime teams`)
- `pip install prime-sandboxes` — lightweight (~50KB) sandbox-only client
- Source: https://github.com/PrimeIntellect-ai/prime

## Open Source

- [`verifiers`](https://github.com/PrimeIntellect-ai/verifiers) — library for RL environments and evaluations
- [`prime-rl`](https://github.com/PrimeIntellect-ai/prime-rl) — agentic RL training at scale
- [`renderers`](https://github.com/PrimeIntellect-ai/renderers) — programmable chat templates for LLM training and inference
- [`research-environments`](https://github.com/PrimeIntellect-ai/research-environments) — environments by the Prime Intellect research team
- [`community-environments`](https://github.com/PrimeIntellect-ai/community-environments) — community-contributed environments
