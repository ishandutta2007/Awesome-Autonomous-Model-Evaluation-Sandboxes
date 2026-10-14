# Awesome-Autonomous-Model-Evaluation-Sandboxes

# Top Autonomous Model Evaluation Sandboxes Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on Multi-Turn Test Cycles, Isolated Evaluation & Agent Observability*  
**Last updated: March 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Autonomous Model Evaluation Sandboxes**. These tools provide isolated environments for running multi-turn AI test cycles—tracing every agent step, scoring outputs with LLM judges, and comparing experiments to catch regressions before they reach production.

**Examples** include Braintrust, LangSmith, DeepEval, Arize Phoenix, Ragas, TruLens, Galileo, Patronus AI, Humanloop, and Fiddler AI (the category leaders).

**Open-source emphasis**: This section is heavily expanded with every major active project for self-hosting, OpenTelemetry-native tracing, and open evaluation frameworks—ideal for AI engineers, platform teams, and developers seeking transparent, vendor-independent model evaluation.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **[Braintrust](https://www.braintrust.dev/)**  
  End-to-end AI product platform combining logging, evaluation datasets, prompt management, and AI proxy with automatic caching and fallback. Trusted by Notion, Stripe, Vercel, Dropbox, and Coursera. **Freemium**: Starter plan free (1 GB logs/month, 14-day retention, 10k eval runs/month), Pro at $249/month (5 GB, 30-day retention, 50k evals), Enterprise with self-hosted/BYOC options . Framework-agnostic with 50+ integrations including OpenAI, Anthropic, LangChain, CrewAI, and OpenTelemetry . **AI-assisted Loop Agent** automates optimization of prompts and evaluations .

- **[LangSmith](https://smith.langchain.com/)**  
  LangChain's observability and evaluation platform with detailed tracing of every LLM call, chain execution, and agent step—showing inputs, outputs, latency, token usage, and cost. Most comprehensive debugging tool for LangChain-based applications . **Free Developer plan** (1 seat, 5k base traces/month), **Plus at $39/seat/month** (10k base traces, 1 free serverless deployment), Enterprise with self-hosted/hybrid options . **Note**: LangSmith is **not fully open source**—it is a hosted, commercial product with a generous free tier . Self-hosted option available as Enterprise add-on running in your Kubernetes cluster .

- **[Galileo](https://galileo.ai/)**  
  Enterprise AI evaluation and observability platform with Experiments API, Groups API, and Integrations API. Provides systematic evaluation workflows for production AI systems .

- **[Humanloop](https://humanloop.com/)**  
  LLM Evals Platform for Enterprises with prompt engineering, evaluation, and observability. **Free tier**: 2 members, 50 eval runs, 10K logs/month. Enterprise adds SSO+SAML, RBAC, VPC deployment, and SLAs. Supports both UI-first and code-first workflows for technical and non-technical team members .

- **[Patronus AI](https://www.patronus.ai/)**  
  Hosted evaluation API running configurable evaluators for hallucination (Lynx), toxicity, PII, prompt injection, and custom judging. Single `/v1/evaluate` endpoint runs multiple evaluators per request with pass/fail verdicts and explanations. **Free Developer tier** with starter credit .

- **[Fiddler AI](https://www.fiddler.ai/)**  
  Enterprise AI observability and model performance monitoring with explainability, bias detection, and LLM evaluation. **Experiments** feature supports A/B testing prompts, model version comparison, regression testing, safety validation, and RAG system evaluation using RAG Health Metrics (AnswerRelevance, ContextRelevance, RAGFaithfulness) .

## Open-Source GitHub Projects

- **[DeepEval](https://github.com/confident-ai/deepeval)**  
  Simple-to-use open-source LLM evaluation framework (Apache-2.0), similar to Pytest but specialized for unit testing LLM outputs. **The most practical open-source eval framework for CI/CD integration** . Features **large variety of ready-to-use metrics** powered by ANY LLM or local NLP models: G-Eval, Summarization, Answer Relevancy, Faithfulness, Contextual Recall, Contextual Precision, RAGAS, Hallucination, Toxicity, Bias. **Red teaming** for 40+ safety vulnerabilities with 10+ attack enhancement strategies. Evaluate entire datasets in bulk in under 20 lines of Python code in parallel. Integrates seamlessly with **ANY CI/CD environment**. Create custom metrics by inheriting base metric class. Benchmarks any LLM on MMLU, HellaSwag, BIG-Bench Hard, TruthfulQA, HumanEval, GSM8K in under 10 lines of code. Optional Confident AI cloud integration for logging, tracing, and production evaluation .

- **[Arize Phoenix](https://github.com/Arize-ai/phoenix)**  
  Open-source AI observability platform (Elastic License 2.0) designed for experimentation, evaluation, and troubleshooting . Features **tracing** via OpenTelemetry-based instrumentation, **evaluation** using LLMs to benchmark performance, **datasets** for versioned examples, **experiments** for tracking prompt/model/retrieval changes, **playground** for prompt optimization and model comparison, and **prompt management** with version control. Vendor and language agnostic with out-of-the-box support for LlamaIndex, LangChain, Haystack, DSPy, smolagents, and LLM providers including OpenAI, Bedrock, MistralAI, VertexAI, LiteLLM, and Google GenAI . Runs practically anywhere: local machine, Jupyter notebook, containerized deployment, or cloud . **2.5M+ monthly downloads**, **10,800+ GitHub stars** .

- **[Ragas](https://github.com/vibrantlabsai/ragas)**  
  Open-source toolkit for evaluating and optimizing LLM applications (Apache-2.0). **The leading open-source RAG evaluation framework** . Features **objective metrics** (LLM-based and traditional), **test data generation** (automatically create comprehensive test datasets covering wide range of scenarios), **seamless integrations** with LangChain and major observability tools, and **feedback loops** leveraging production data. Install via `pip install ragas`. CLI quickstart: `ragas quickstart rag_eval` creates complete RAG evaluation project .

- **[TruLens](https://github.com/truera/trulens)**  
  Open-source evaluation and tracing framework (Apache-2.0). **OpenTelemetry-native**—instrument any app with a decorator, score every step with LLM judges that explain themselves, compare versions, and ship the one that earns it . Features **trace every step** (latency, inputs, outputs, tokens, cost recorded per step), **compare versions** (scores, latency, cost per app version), **seven purpose-built evaluators for agentic systems** (LogicalConsistency, ExecutionEfficiency, PlanAdherence, PlanQuality, ToolSelection, etc.). Judges are graded against human annotations out of the box: **95% agent errors caught with Agent GPA on TRAIL/GAIA** (vs 55% baseline), **0.81 Groundedness F1 on LLM-AggreFact**, **0.93 Context relevance NDCG@5** . Adopted by Walmart Global Tech, Cisco, J.P. Morgan Chase, Equinix, VMware by Broadcom, Hitachi Digital Services, Thomson Reuters . Tracing is OpenTelemetry-native—portable to any OTLP backend (Jaeger, Grafana Tempo, Datadog) .

- **[Braintrust Go SDK](https://github.com/braintrustdata/braintrust-x-go)**  
  Open-source Go SDK for Braintrust (Apache-2.0) in BETA status. Features evaluations with custom scoring functions, automatic instrumentation for OpenAI and Anthropic API calls, datasets management and versioning, experiments tracking, and production observability . **Note**: SDK is open-source; the Braintrust platform itself is commercial SaaS with self-hosted options on Enterprise .

- **[Promptfoo](https://github.com/promptfoo/promptfoo)**  
  Open-source LLM testing and red-teaming framework (MIT). **20,000+ GitHub stars**. Listed as one of five tools people actually use for LLM evaluation alongside Braintrust, LangSmith, Inspect, and Ragas . OpenAI announced acquisition in March 2026 with commitment to keep the open-source project going.

### Additional Strong Open-Source Options

- **[Inspect](https://github.com/UKGovernmentBEIS/inspect_ai)** — Open-source framework for large language model evaluations from UK AI Safety Institute. Listed as one of five tools people actually use for LLM evaluation .
- **[Langfuse](https://github.com/langfuse/langfuse)** — Open-source LLM engineering platform (MIT core) with tracing, evaluations, prompt management, and datasets. **35,000+ GitHub stars**. Self-hostable. **Acquired by ClickHouse in January 2026 with commitment to keep it open source** .
- **[Comet Opik](https://github.com/comet-ml/opik)** — Fully-permissive Apache-2.0 rival to Langfuse. **22,000+ GitHub stars**. Full platform—backend included—free to self-host. Covers AI agent tracing, LLM evaluation, prompt optimization, production monitoring, and Opik Guardrails.
- **[OpenLLMetry (Traceloop)](https://github.com/traceloop/openllmetry)** — Apache-2.0 OpenTelemetry instrumentation for LLM providers, vector DBs, and frameworks. Emits standard `gen_ai` spans portable to any OTel backend .
- Community **n8n** workflows for evaluation alerting and regression detection automation.

**Frameworks for building custom systems**: Combine **DeepEval** for CI/CD-integrated test cycles with **Arize Phoenix** for OpenTelemetry-native tracing and experiments, **TruLens** for agentic evaluation and version comparison, **Ragas** for RAG-specific metrics, and **ClickHouse/PostgreSQL** for trace storage—creating a fully self-hosted, enterprise-grade model evaluation platform.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Model evaluation platforms handling prompts and traces must comply with data protection regulations (GDPR, CCPA, etc.), especially when traces contain PII.
- **"Open source" means different things in this category.** DeepEval, Ragas, and TruLens are genuinely open source (Apache-2.0). Arize Phoenix uses Elastic License 2.0 (source-available, not OSI-approved). LangSmith is closed SaaS with open SDKs and Enterprise self-hosting. Braintrust is closed SaaS with open SDKs and Enterprise self-hosting. **Check the LICENSE file, not the marketing page** .
- **Self-hosting is a hard requirement when prompts or traces carry regulated data.** If they do, the field collapses to DeepEval, Phoenix, Ragas, TruLens, Langfuse, Opik, and OpenLLMetry. LangSmith and Braintrust cannot self-host on lower tiers .
- **Observability is not evaluation.** Tracing tells you what happened; evaluation tells you whether it was good. Most tools ship both—which makes it easy to buy one and never configure the other. Tracing alone will not catch quality drift.
- Self-hosted open-source solutions require proper security hardening, LLM infrastructure (or API keys), and ongoing maintenance. Evaluation judges are themselves LLMs—their scores are probabilistic and should be validated against human annotations for high-stakes decisions.

---

**Made for AI engineers, platform teams, and developers building transparent model evaluation solutions.**  
Let's make Autonomous Model Evaluation Sandboxes more open, data-driven, and reliable.
