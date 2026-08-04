# UpTrain (uptrain)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
