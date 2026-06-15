# Prime Intellect (prime-intellect)

Prime Intellect is a San Francisco–based startup building an open and decentralized stack for developing and improving AI agents through reinforcement learning. The company combines a 50+ provider GPU compute marketplace (single-node and 1–256 GPU multi-node clusters across H100, H200, B200, and B300), a managed RL post-training service ("Lab") that fine-tunes Qwen3.5, Llama, NVIDIA Nemotron, and OpenAI gpt-oss base models against a 2,500+ environment library (the Environments Hub), secure remote Python sandboxes for agent code execution, OpenAI-compatible inference at api.pinference.ai with LoRA adapter deployments, and an evaluations service that runs against the same environments. Prime Intellect is also the publisher of INTELLECT-3 (100B+ MoE trained with RL), INTELLECT-2 (32B trained via distributed RL), and the SYNTHETIC-2 dataset of four million reasoning traces, and develops the open-source `verifiers` RL library and the `prime-rl` async RL training framework. Everything is exposed via a single bearer-token REST API at api.primeintellect.ai, a `prime` Python CLI/SDK (PyPI: `prime`, lightweight `prime-sandboxes`), and the OpenAI protocol on the inference plane.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/prime-intellect/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/prime-intellect/refs/heads/main/apis.yml)

## Scope

- **Type:** Index
- **Position:** Provider
- **Access:** 3rd-Party

## Tags

- AI
- Artificial Intelligence
- Reinforcement Learning
- GPU Compute
- Decentralized Compute
- Foundation Models
- Inference
- Sandboxes
- Training
- Environments
- Evaluations
- LoRA
- Open Source
- Agents

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## APIs

### Prime Intellect Compute API

Programmatic access to the Prime Intellect compute marketplace. Query GPU availability across 50+ providers, provision and manage on-demand or multi-node GPU pods (1-256 GPUs across H100, H200, B200, B300, A100), attach persistent network disks, and manage SSH keys for pod access. Backs the `prime pods`, `prime availability`, and `prime disks` CLI commands.

- **Human URL:** [https://docs.primeintellect.ai/api-reference/managing-pods](https://docs.primeintellect.ai/api-reference/managing-pods)
- **Base URL:** `https://api.primeintellect.ai`

#### Tags

- GPU Compute
- Marketplace
- Pods
- Disks
- SSH Keys
- Availability

#### Properties

- [Documentation](https://docs.primeintellect.ai/api-reference/introduction)
- [Documentation](https://docs.primeintellect.ai/api-reference/managing-pods)
- [Documentation](https://docs.primeintellect.ai/api-reference/managing-disks)
- [Documentation](https://docs.primeintellect.ai/api-reference/check-gpu-availability)
- [OpenAPI](openapi/prime-intellect-compute-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/prime-intellect-compute-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/prime-intellect-compute-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/prime-intellect-pod-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON-LD](json-ld/prime-intellect-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)

### Prime Intellect Sandbox API

Secure remote code-execution sandboxes for AI agents. Create and manage Python-3.11-slim-based sandboxes, expose ports for HTTP services running inside the sandbox, open SSH sessions, pull rich error context for failures, and provision reverse tunnels back into a sandbox from an external network. Available as a lightweight `prime-sandboxes` Python package (~50KB) in addition to the full `prime` CLI/SDK.

- **Human URL:** [https://docs.primeintellect.ai/sandboxes/overview](https://docs.primeintellect.ai/sandboxes/overview)
- **Base URL:** `https://api.primeintellect.ai`

#### Tags

- Sandbox
- Code Execution
- Agents
- Tunnels

#### Properties

- [Documentation](https://docs.primeintellect.ai/sandboxes/overview)
- [Documentation](https://docs.primeintellect.ai/sandboxes/sdk)
- [Documentation](https://docs.primeintellect.ai/sandboxes/cli)
- [Documentation](https://docs.primeintellect.ai/sandboxes/tunnel)
- [OpenAPI](openapi/prime-intellect-sandbox-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/prime-intellect-sandbox-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/prime-intellect-sandbox-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/prime-intellect-sandbox-schema.json) — [JSON Schema](https://json-schema.org/specification)

### Prime Intellect Training API

Hosted reinforcement-learning post-training service ("Lab"). Launch dedicated training runs against a catalog of base models — Qwen3.5 (0.8B through 397B-A17B), Llama 1B/3B Instruct, NVIDIA Nemotron 30B/120B, OpenAI gpt-oss 20B/120B — drive them with environments from the Environments Hub, and retrieve token-level usage + USD cost per run from the billing endpoints. Pricing is per-million-token across separate input, output, and training meters.

- **Human URL:** [https://docs.primeintellect.ai/hosted-training/what-is-lab](https://docs.primeintellect.ai/hosted-training/what-is-lab)
- **Base URL:** `https://api.primeintellect.ai`

#### Tags

- Reinforcement Learning
- Training
- Fine-Tuning
- Foundation Models
- Billing

#### Properties

- [Documentation](https://docs.primeintellect.ai/hosted-training/what-is-lab)
- [Documentation](https://docs.primeintellect.ai/hosted-training/getting-started)
- [Documentation](https://docs.primeintellect.ai/hosted-training/end-to-end-run)
- [Pricing](https://docs.primeintellect.ai/hosted-training/models-and-pricing)
- [OpenAPI](openapi/prime-intellect-training-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/prime-intellect-training-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/prime-intellect-training-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/prime-intellect-training-run-schema.json) — [JSON Schema](https://json-schema.org/specification)

### Prime Intellect Evaluations API

Create, manage, and submit samples to evaluations against the Prime Intellect Environments Hub (2,500+ RL environments). Supports both client-driven evaluations (push samples, finalize, retrieve) and fully hosted evaluations executed by Prime Intellect with logs, cancellation, and selectable inference models. Backs `prime eval` CLI commands.

- **Human URL:** [https://docs.primeintellect.ai/tutorials-environments/hosted-evaluations](https://docs.primeintellect.ai/tutorials-environments/hosted-evaluations)
- **Base URL:** `https://api.primeintellect.ai`

#### Tags

- Evaluations
- Benchmarks
- Reinforcement Learning
- Environments

#### Properties

- [Documentation](https://docs.primeintellect.ai/tutorials-environments/environments)
- [Documentation](https://docs.primeintellect.ai/tutorials-environments/evaluating)
- [Documentation](https://docs.primeintellect.ai/tutorials-environments/hosted-evaluations)
- [OpenAPI](openapi/prime-intellect-evaluations-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/prime-intellect-evaluations-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/prime-intellect-evaluations-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/prime-intellect-evaluation-schema.json) — [JSON Schema](https://json-schema.org/specification)

### Prime Intellect Inference API

OpenAI-compatible inference API for hosted frontier and open models served at api.pinference.ai. Supports streaming chat completions, the full set of OpenAI parameters (temperature, top_p, max_tokens, logprobs), and returns a `usage` object with input/output token counts and USD cost on every response. LoRA adapters can be served alongside base models via 1-click deployments.

- **Human URL:** [https://docs.primeintellect.ai/inference/overview](https://docs.primeintellect.ai/inference/overview)
- **Base URL:** `https://api.pinference.ai/api/v1`

#### Tags

- Inference
- OpenAI Compatible
- Foundation Models
- LLM

#### Properties

- [Documentation](https://docs.primeintellect.ai/inference/overview)
- [Documentation](https://docs.primeintellect.ai/inference/usage)
- [Documentation](https://docs.primeintellect.ai/inference/adapter-deployments)
- [OpenAPI](openapi/prime-intellect-inference-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/prime-intellect-inference-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/prime-intellect-inference-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Prime Intellect Platform API

Account, team, secrets, image, and cluster administration. Whoami and team membership, secret CRUD for use inside pods and sandboxes, Docker image builds with public/private visibility, registry credential checks, FRP plugin validation, and admin-only cluster + node-log endpoints.

- **Human URL:** [https://docs.primeintellect.ai/api-reference/teams](https://docs.primeintellect.ai/api-reference/teams)
- **Base URL:** `https://api.primeintellect.ai`

#### Tags

- Account
- Teams
- Secrets
- Images
- Administration

#### Properties

- [Documentation](https://docs.primeintellect.ai/api-reference/teams)
- [Authentication](https://docs.primeintellect.ai/api-reference/api-keys)
- [OpenAPI](openapi/prime-intellect-platform-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/prime-intellect-platform-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/prime-intellect-platform-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Website](https://www.primeintellect.ai)
- [Documentation](https://docs.primeintellect.ai)
- [Portal](https://app.primeintellect.ai)
- [API Reference](https://docs.primeintellect.ai/api-reference/introduction)
- [OpenAPI](https://api.primeintellect.ai/openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Authentication](https://docs.primeintellect.ai/api-reference/api-keys)
- [C L I](https://docs.primeintellect.ai/cli-reference/introduction)
- [SDK](https://github.com/PrimeIntellect-ai/prime)
- [SDK](https://pypi.org/project/prime/)
- [SDK](https://pypi.org/project/prime-sandboxes/)
- [Open Source](https://github.com/PrimeIntellect-ai/verifiers)
- [Open Source](https://github.com/PrimeIntellect-ai/prime-rl)
- [Open Source](https://github.com/PrimeIntellect-ai/renderers)
- [Open Source](https://github.com/PrimeIntellect-ai/research-environments)
- [Open Source](https://github.com/PrimeIntellect-ai/community-environments)
- [Git Hub](https://github.com/PrimeIntellect-ai)
- [Hugging Face](https://huggingface.co/PrimeIntellect)
- [Blog](https://www.primeintellect.ai/blog)
- [Pricing](https://docs.primeintellect.ai/hosted-training/models-and-pricing)
- [Plans](plans/prime-intellect-plans-pricing.yml)
- [Rate Limits](rate-limits/prime-intellect-rate-limits.yml)
- [Fin Ops](finops/prime-intellect-finops.yml)
- [Discord](https://discord.gg/primeintellect)
- [Twitter](https://x.com/PrimeIntellect)
- [LinkedIn](https://www.linkedin.com/company/primeintellect-ai)
- [Events](https://luma.com/primeintellect)
- [Careers](https://jobs.ashbyhq.com/PrimeIntellect)
- [Contact](https://www.primeintellect.ai/contact)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
