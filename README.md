# UpTrain (uptrain)

UpTrain is an open-source (Apache-2.0) unified platform to evaluate and improve generative AI and LLM applications. It ships a Python framework plus a managed evaluation API that grades responses against 20+ preconfigured checks - context relevance, factual accuracy, response completeness, hallucination, tonality, prompt injection and more - and performs root cause analysis on failure cases.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/uptrain/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/uptrain/refs/heads/main/apis.yml)

## Tags

- AI
- LLM
- Evaluation
- LLM Evaluation
- Observability
- Open Source

## Timestamps

- **Created:** 2026-06-20
- **Modified:** 2026-06-20

## APIs

### UpTrain Evaluations API

Runs evaluations (POST /evaluate) on supplied LLM input/output/context rows against a list of named checks such as context_relevance, factual_accuracy, response_completeness and response_conciseness, returning per-row grades and explanations. Authenticated with an uptrain-access-token header.

- **Human URL:** [https://docs.uptrain.ai/](https://docs.uptrain.ai/)
- **Base URL:** `https://demo.uptrain.ai/api/public`

#### Tags

- Evaluation
- LLM
- Checks

#### Properties

- [Documentation](https://docs.uptrain.ai/getting-started/introduction)
- [API Reference](https://docs.uptrain.ai/predefined-evaluations/overview)
- [OpenAPI](openapi/uptrain-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/uptrain.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/uptrain.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### UpTrain Log and Evaluate API

Logs evaluation data under a named project and evaluates it in one call (POST /log_and_evaluate), persisting results so they appear on the managed UpTrain dashboard with real-time monitoring. The same endpoint backs evaluate_experiments for A/B comparison of prompt or model variants.

- **Human URL:** [https://docs.uptrain.ai/](https://docs.uptrain.ai/)
- **Base URL:** `https://demo.uptrain.ai/api/public`

#### Tags

- Logging
- Evaluation
- Projects

#### Properties

- [Documentation](https://docs.uptrain.ai/getting-started/quickstart)
- [OpenAPI](openapi/uptrain-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/uptrain.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/uptrain.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### UpTrain Root Cause Analysis API

Performs root cause analysis (POST /perform_root_cause_analysis) on failing RAG or LLM responses, classifying why a response was poor - e.g. incomplete context, poor retrieval, or hallucination - to guide remediation.

- **Human URL:** [https://docs.uptrain.ai/](https://docs.uptrain.ai/)
- **Base URL:** `https://demo.uptrain.ai/api/public`

#### Tags

- Root Cause Analysis
- RAG
- Diagnostics

#### Properties

- [Documentation](https://docs.uptrain.ai/predefined-evaluations/overview)
- [OpenAPI](openapi/uptrain-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/uptrain.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/uptrain.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### UpTrain Runs and Datasets API

Manages evaluation datasets, checksets (reusable bundles of checks), and runs that pair a dataset with a checkset - create a run (POST /run), poll its status (GET /run/{run_id}) and download its results (GET /run/{run_id}/results).

- **Human URL:** [https://docs.uptrain.ai/](https://docs.uptrain.ai/)
- **Base URL:** `https://demo.uptrain.ai/api/public`

#### Tags

- Runs
- Datasets
- Checksets

#### Properties

- [Documentation](https://docs.uptrain.ai/getting-started/quickstart)
- [OpenAPI](openapi/uptrain-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/uptrain.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/uptrain.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [GitHub Organization](https://github.com/uptrain-ai)
- [LinkedIn](https://www.linkedin.com/company/uptrain-ai)
- [Website](https://uptrain.ai/)
- [Documentation](https://docs.uptrain.ai/)
- [Plans](plans/uptrain-plans-pricing.yml)
- [Rate Limits](rate-limits/uptrain-rate-limits.yml)
- [Fin Ops](finops/uptrain-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
