# Awesome AI PHP [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

A curated list of **PHP** libraries, SDKs, frameworks, and software for **Artificial Intelligence**, **LLMs**, **Machine Learning**, and **Agentic AI**.

> PHP is evolving. With modern asynchronous frameworks and robust type systems, it's becoming a solid choice for orchestrating AI agents and integrating LLMs into business logic.

## Contents

- [Large Language Models (LLMs)](#large-language-models-llms)
- [Framework Integrations](#framework-integrations)
- [Agentic AI & Frameworks](#agentic-ai--frameworks)
- [AI Protocols (MCP, A2A)](#ai-protocols-mcp-a2a)
- [Local Models & Inference](#local-models--inference)
- [Machine Learning](#machine-learning)
- [Vector Databases](#vector-databases)
- [RAG & Embeddings](#rag--embeddings)
- [Natural Language Processing (NLP)](#natural-language-processing-nlp)
- [Computer Vision](#computer-vision)
- [Voice & Audio](#voice--audio)
- [Infrastructure & Cloud AI](#infrastructure--cloud-ai)
- [Evaluation & Observability](#evaluation--observability)
- [Learning Resources](#learning-resources)
- [Regulation, Governance & Standards for AI](#regulation-governance--standards-for-ai)
- [Security & Safety for AI](#security--safety-for-ai)

---

## Large Language Models (LLMs)
*Clients and SDKs for popular LLM providers.*

- [**openai-php/client**](https://github.com/openai-php/client) - A supercharged community-maintained PHP client for the OpenAI API. The de-facto standard; also supports Azure OpenAI.
- [**gemini-api-php/client**](https://github.com/gemini-api-php/client) - PHP client for the Gemini AI API.
- [**google-gemini-php/client**](https://github.com/google-gemini-php/client) - Alternative community PHP client for Gemini AI (separate project, maintained independently).
- [**ArdaGnsrn/ollama-php**](https://github.com/ArdaGnsrn/ollama-php) - PHP library for Ollama, enabling local LLM execution.
- *Note*: For **Anthropic Claude**, **Mistral**, and **DeepSeek**, the recommended approach is the unified abstractions provided by [Laravel AI](#laravel) or [Prism](#laravel), which maintain up-to-date provider drivers without requiring standalone clients.

## Framework Integrations
*AI tools tailored for specific PHP frameworks.*

### Laravel
- [**laravel/ai**](https://github.com/laravel/ai) - The **official** Laravel first-party AI SDK (v0.7.0, May 2026). Unified API for OpenAI, Anthropic, Gemini, and more; agents, tool use, image generation, audio, embeddings, and RAG built in.
- [**Prism**](https://prismphp.com/) - A unified LLM package for Laravel that abstracts provider differences (OpenAI, Anthropic, Gemini, Ollama, Groq, and more). Rapidly becoming the standard multi-provider abstraction layer.
  - [GitHub](https://github.com/prism-php/prism)
- [**openai-php/laravel**](https://github.com/openai-php/laravel) - Official-ish Laravel wrapper for the OpenAI PHP client.
- [**LarAgent**](https://github.com/MaestroError/LarAgent) - Eloquent-style agent framework for Laravel: tools, memory, multi-agent workflows, and structured output.
- [**cloudstudio/ollama-laravel**](https://github.com/cloudstudio/ollama-laravel) - First-class Laravel integration for Ollama with streaming, function calling, thinking-model support, and embeddings. Requires PHP 8.2+ / Laravel 11+.
- [**neuron-ai/neuron-laravel**](https://neuron-ai.dev/) - Laravel adapter for the Neuron AI agentic framework.

### Symfony
- [**symfony/ai**](https://github.com/symfony/ai) - **Official** Symfony AI components for building AI-enabled applications. Covers LLMs, embeddings, agents, vector stores, MCP, and more. (Absorbed the former `php-llm/llm-chain` project.)
- [**symfony/mcp-bundle**](https://github.com/symfony/mcp-bundle) - Official Symfony bundle for building MCP servers, part of the `symfony/ai` initiative.

### Yii & Other Frameworks
- [**ldkafka/yii2-google-gemini**](https://github.com/ldkafka/yii2-google-gemini) - Gemini AI integration for Yii2.
- *General Note*: Most generic PHP clients (like `openai-php/client`) work seamlessly in any PHP framework.

## Agentic AI & Frameworks
*Frameworks for building autonomous agents, reasoning engines, and complex AI applications.*

- [**Neuron AI**](https://neuron-ai.dev/) - Full-featured agentic framework for PHP. Build autonomous agents that can plan, use tools, search data, and interact with multiple LLM providers (OpenAI, Anthropic, Ollama, etc.).
  - [GitHub](https://github.com/neuron-core/neuron-ai)
- [**LarAgent**](https://github.com/MaestroError/LarAgent) - Eloquent-style agent framework for Laravel with tools, memory, multi-agent workflows, and structured output.
- [**Utopia Agents**](https://github.com/utopia-php/agents) - Lightweight, framework-agnostic library for creating and orchestrating AI agents. Supports multiple providers, optimized for performance. Maintained by the Appwrite team.
- [**LLPhant**](https://github.com/LLPhant/LLPhant) - Comprehensive Generative AI framework for PHP, heavily inspired by LangChain. Supports OpenAI, Anthropic, Ollama, and vector stores.
- [**Resonance**](https://github.com/distantmagic/resonance) - Asynchronous PHP framework optimized for IO-intensive tasks, used for serving ML models and high-concurrency agent backends. *(no commits since Dec 2024)*

### Agentic Patterns
- **RAG (Retrieval Augmented Generation)**: Supported out of the box by Neuron AI, LLPhant, Laravel AI, and Prism.
- **Tool Use**: Standardized function exposure to LLMs via JSON schemas; native in all major frameworks above.
- **ReAct (Reason-Act) loops**: Supported by Neuron AI and implementable with LLPhant/LangGraph-style chaining.

## AI Protocols (MCP, A2A)
*Implementations of modern AI communication protocols.*

### Model Context Protocol (MCP)
*Standard for connecting AI models to external data and tools.*
- [**php-mcp/server**](https://github.com/php-mcp/server) - Standalone PHP MCP Server SDK. Attribute-based element discovery, PSR-11 DI, stdio/HTTP/streamable-HTTP transports.
- [**php-mcp/client**](https://github.com/php-mcp/client) - Standalone PHP MCP Client SDK. ReactPHP async + sync APIs, PSR-3/16/14 compliant.
- [**php-mcp/laravel**](https://github.com/php-mcp/laravel) - Laravel-native SDK for building MCP servers. Exposes Tools, Resources, and Prompts via PHP attributes with deep Laravel service container/cache/Artisan integration.
- [**symfony/mcp-bundle**](https://github.com/symfony/mcp-bundle) - Official Symfony bundle for MCP, part of the `symfony/ai` initiative.
- [**Logiscape/mcp-sdk-php**](https://github.com/Logiscape/mcp-sdk-php) - Complete SDK for building both MCP Clients and Servers.
- [**swisnl/mcp-client**](https://github.com/swisnl/mcp-client) - Asynchronous PHP client for the Model Context Protocol.
- [**james2037/mcp-php-server**](https://github.com/james2037/mcp-php-server) - Focused MCP Server implementation.

### Agent-to-Agent (A2A) Protocol
*Protocol for seamless communication between autonomous agents.*
- [aurimasbutkus/a2a-php](https://github.com/aurimasbutkus/a2a-php) - Framework-agnostic A2A protocol implementation.
- [**andreibesleaga/a2a-php**](https://github.com/andreibesleaga/a2a-php) - A comprehensive PHP implementation of the A2A protocol (v0.3).

## Local Models & Inference
*Run AI models locally within PHP without external API calls.*

- [**TransformersPHP**](https://github.com/CodeWithKyrian/transformers-php) - PHP port of HuggingFace Transformers running over ONNX Runtime via FFI. Supports 30+ architectures: NLP, vision, embeddings, and multimodal inference entirely in-process. The cornerstone of local PHP AI.
  - `composer require codewithkyrian/transformers`
- [**cloudstudio/ollama-laravel**](https://github.com/cloudstudio/ollama-laravel) - Laravel integration for Ollama (local LLM server). Streaming, function calling, thinking-model support. See also [Framework Integrations](#framework-integrations).
- [**ArdaGnsrn/ollama-php**](https://github.com/ArdaGnsrn/ollama-php) - Framework-agnostic PHP library for Ollama.

## Machine Learning
*Core libraries for training and running ML models in PHP.*

- [**Rubix ML**](https://github.com/RubixML/ML) - A high-level machine learning and deep learning library for PHP. Supports nearly every ML task from classification/regression to clustering and anomaly detection.

## Vector Databases
*PHP clients for vector stores, essential for RAG (Retrieval-Augmented Generation).*

- [**hkulekci/qdrant-php**](https://github.com/hkulekci/qdrant-php) - PHP Client for Qdrant Vector Database.
- [**timkley/weaviate-php**](https://github.com/timkley/weaviate-php) - PHP Client for Weaviate.
- [**CodeWithKyrian/chromadb-php**](https://github.com/CodeWithKyrian/chromadb-php) - ChromaDB client for PHP.
- [**probots-io/pinecone-php**](https://github.com/probots-io/pinecone-php) - PHP client for Pinecone.
- [**typesense/typesense-php**](https://github.com/typesense/typesense-php) - Official PHP client for Typesense, which supports native vector and hybrid semantic search.

## RAG & Embeddings
*Tools for building Retrieval-Augmented Generation pipelines in PHP.*

- [**tpetry/laravel-postgresql-enhanced**](https://github.com/tpetry/laravel-postgresql-enhanced) - Extends Laravel's Postgres driver with first-class pgvector support (`vector()` column type, `orderByVectorSimilarity()` for cosine/L2 distance). The practical pgvector answer for Laravel RAG pipelines.
- [**laravel/ai**](https://github.com/laravel/ai) - Official Laravel AI SDK includes native embeddings and RAG pipeline support.
- [**LLPhant**](https://github.com/LLPhant/LLPhant) - Includes a full RAG pipeline with document loaders, splitters, embeddings, and vector store integrations.
- [**Neuron AI**](https://github.com/neuron-core/neuron-ai) - Built-in RAG support with tool-use integration.
- [**TransformersPHP**](https://github.com/CodeWithKyrian/transformers-php) - Generate embeddings locally without API calls via ONNX-backed transformer models.

## Natural Language Processing (NLP)
*Tools for processing and analyzing text.*

- [**patrickschur/language-detection**](https://github.com/patrickschur/language-detection) - A language detection library for PHP supporting 60+ languages.

## Computer Vision
*Image processing and vision capabilities.*

- [**Google Cloud Vision PHP**](https://github.com/googleapis/google-cloud-php-vision) - Official Google Cloud Vision API client for PHP (part of `googleapis/google-cloud-php` monorepo).
- *Note*: For Azure Computer Vision and AWS Rekognition, use the respective cloud SDKs (`aws/aws-sdk-php` and Azure REST clients) — no dedicated official PHP wrapper exists for these services.

## Voice & Audio
*Speech-to-Text (STT) and Text-to-Speech (TTS).*

- [**openai-php/client**](https://github.com/openai-php/client) - Supports OpenAI's Whisper model for transcription and TTS via `audio()->transcribe()` and `audio()->speech()`.
- [**runapi-ai/elevenlabs-php**](https://github.com/runapi-ai/elevenlabs-php) - Composer package for ElevenLabs text-to-speech, dialogue generation, sound effects, transcription, and audio isolation workflows through RunAPI.
- *Note*: For AssemblyAI and Deepgram, no official PHP SDKs currently exist. These services expose REST APIs consumable via PHP HTTP clients (Guzzle, Symfony HttpClient).

## Infrastructure & Cloud AI
*SDKs and tools for deploying AI on major cloud providers and specialized infrastructure.*

### AWS (Amazon Web Services)
- [**aws/aws-sdk-php**](https://github.com/aws/aws-sdk-php) - Official AWS SDK for PHP. Supports **Amazon Bedrock** (serverless LLMs), **SageMaker**, and Bedrock Guardrails via `BedrockRuntimeClient`.

### Google Cloud Platform (GCP)
- [**google-gemini-php/client**](https://github.com/google-gemini-php/client) - Community PHP client for Gemini AI with streaming support.
- [**gemini-api-php/client**](https://github.com/gemini-api-php/client) - Alternative PHP client for the Gemini AI API.
- *Note*: Google does not provide an official PHP SDK for Vertex AI. Use the REST API directly via HTTP clients or consider the Python/Node SDK behind a microservice boundary.

### Azure (Microsoft)
- [**openai-php/client**](https://github.com/openai-php/client) - The recommended client for connecting to **Azure OpenAI** endpoints.
- *Note*: No official Azure Content Safety PHP SDK exists. Use the Azure REST API directly for content moderation.

### Hugging Face & Replicate
- *Note*: Both `mateffy/huggingface` and the previously listed Replicate PHP clients are no longer maintained. For Hugging Face cloud inference, use the REST API directly or run models locally via [TransformersPHP](#local-models--inference). For Replicate, the REST API is straightforward to call via any PHP HTTP client.

## Evaluation & Observability
*Tools for testing, evaluating, and monitoring AI applications.*

- *Gap*: No PHP-native LLM evaluation or tracing library currently exists on Packagist. **Contributions welcome.**
- [**Promptfoo**](https://promptfoo.dev/docs/red-team/) - JS/CLI-based LLM eval and red-team tool; runnable from PHP CI/CD pipelines as a CLI subprocess.
- [**Langfuse**](https://langfuse.com/) - Open-source LLM engineering platform. No official PHP SDK, but fully accessible via its REST API from any PHP HTTP client.
- [**LangSmith**](https://smith.langchain.com/) - LangChain's tracing and monitoring platform; usable from PHP apps via the REST API.

---

## Learning Resources
*High-quality tutorials, courses, and guides for building AI with PHP.*

### Courses
- [**AI Machine Learning Complete Course: for PHP & Python Devs**](https://www.udemy.com/course/machine-learning-artificial-intelligence-in-php/) - (Udemy) Covers AI fundamentals, machine learning types, and building AI agents tailored for PHP developers. Updated late 2025.

### Tutorials & Articles
- [**Integrating AI APIs in PHP**](https://phptutorialpoints.in/how-to-integrate-ai-apis-in-php/) - Deep dive into connecting PHP with major AI providers.
- [**Building LLM Applications with PHP**](https://www.bacancytechnology.com/blog/php-and-llm) - Guide on integrating LLMs into PHP apps.

### Community & Documentation
- [**Neuron AI Documentation**](https://docs.neuron-ai.dev/) - Docs for the leading PHP agentic framework.
- [**LLPhant GitHub**](https://github.com/LLPhant/LLPhant) - Source and docs for the LangChain-inspired PHP framework.
- [**PHP Foundation**](https://thephp.foundation/) - Follow for official announcements on PHP language development and ecosystem initiatives.
- [**Prism Documentation**](https://prismphp.com/) - Comprehensive docs for multi-provider LLM abstraction in Laravel.

---

## Regulation, Governance & Standards for AI

### International Frameworks & Declarations

- [**EU AI Act – Official Portal**](https://artificialintelligenceact.eu/) - Comprehensive tracker for Regulation (EU) 2024/1689, the world's first horizontal AI law. Risk-based framework; GPAI obligations applicable since August 2025.
- [**EU AI Act – European Commission**](https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai) - Official Commission overview with compliance timelines and risk-tier definitions.
- [**OECD AI Principles**](https://oecd.ai/en/ai-principles) - Updated May 2024 intergovernmental standard (47 adherents) covering trustworthy AI.
- [**Bletchley Declaration (AI Safety Summit 2023)**](https://www.gov.uk/government/publications/ai-safety-summit-2023-the-bletchley-declaration) - First multilateral declaration on frontier AI risks, signed by 28 countries and the EU.
- [**Seoul Declaration (AI Seoul Summit 2024)**](https://www.gov.uk/government/publications/seoul-declaration-for-safe-innovative-and-inclusive-ai-ai-seoul-summit-2024) - Follow-on commitment extending Bletchley; established the international network of AI Safety Institutes.
- [**Hiroshima AI Process – G7 International Code of Conduct**](https://digital-strategy.ec.europa.eu/en/library/hiroshima-process-international-code-conduct-advanced-ai-systems) - Voluntary G7 code for organisations developing advanced foundation and agentic models.

### National & Regional Governance

- [**UK AI Security Institute (AISI)**](https://www.aisi.gov.uk/) - State-backed institute publishing frontier model evaluations and agentic capability assessments.
- [**Singapore AI Verify Foundation**](https://aiverifyfoundation.sg/) - Open-source AI governance testing framework and toolkit.
- [**Blueprint for an AI Bill of Rights (US OSTP)**](https://bidenwhitehouse.archives.gov/ostp/ai-bill-of-rights/) - Five-principle US OSTP blueprint; widely referenced reference document.
- [**US National AI Legislative Framework (March 2026)**](https://www.whitehouse.gov/releases/2026/03/president-donald-j-trump-unveils-national-ai-legislative-framework/) - Current US federal AI policy framework.

### Standards (NIST, ISO/IEC, IEEE)

- [**NIST AI Risk Management Framework (AI RMF 1.0)**](https://www.nist.gov/itl/ai-risk-management-framework) - Voluntary Govern/Map/Measure/Manage framework with companion Playbook.
- [**NIST AI 600-1 – Generative AI Profile**](https://www.nist.gov/itl/ai-risk-management-framework) - NIST's GenAI-specific companion profile to the AI RMF.
- [**NIST AI 100-2 E2025 – Adversarial ML Taxonomy**](https://csrc.nist.gov/pubs/ai/100/2/e2025/final) - Authoritative taxonomy of adversarial ML attacks and mitigations, including LLM-specific threats.
- **ISO/IEC 42001:2023 – AI Management System** - Certifiable AI management standard. Search "ISO/IEC 42001" at [iso.org](https://www.iso.org/).
- **ISO/IEC 23894:2023 – AI Risk Management** - Companion AI risk-management guidance.
- **ISO/IEC 5338:2023 – AI System Life Cycle Processes** - Life-cycle process standard for AI systems.
- [**IEEE 7000-2021 – Ethical System Design**](https://standards.ieee.org/ieee/7000/6781/) - Process standard for embedding ethical considerations through the system life cycle.

### Industry Frameworks

- [**Frontier Model Forum**](https://www.frontiermodelforum.org/) - Industry body (Amazon, Anthropic, Google, Meta, Microsoft, OpenAI) coordinating frontier safety best practices.
- [**Anthropic Responsible Scaling Policy**](https://www.anthropic.com/news/anthropics-responsible-scaling-policy) - AI Safety Levels (ASL) framework defining capability thresholds and safeguards for agentic deployments.
- [**Google DeepMind Frontier Safety Framework**](https://deepmind.google/discover/blog/introducing-the-frontier-safety-framework/) - Critical Capability Levels covering autonomy, biosecurity, and cybersecurity.
- [**METR (formerly ARC Evals)**](https://metr.org/) - Independent nonprofit evaluating autonomous and agentic capabilities of frontier models.
- [**Center for AI Safety (CAIS)**](https://safe.ai/) - Research and field-building nonprofit focused on societal-scale AI risks.

---

## Security & Safety for AI

### OWASP Resources

- [**OWASP Top 10 for LLM Applications (2025)**](https://genai.owasp.org/llm-top-10/) - Latest 2025 list (LLM01 Prompt Injection through LLM10 Unbounded Consumption). **LLM06 Excessive Agency** directly addresses agentic risk. Framework-agnostic — fully applicable to PHP LLM applications.
- [**OWASP Agentic Security Initiative**](https://genai.owasp.org/initiatives/agentic-security-initiative/) - Includes the **OWASP Top 10 for Agentic Applications 2026**, the Practical Guide for Secure MCP Server Development, and the FinBot agentic CTF.
- [**OWASP AI Exchange**](https://owaspai.org/) - 300+ pages of AI security guidance and a "periodic table" of AI threats and controls, aligned with the EU AI Act and ISO standards.
- [**OWASP LLM Applications Cybersecurity & Governance Checklist**](https://genai.owasp.org/resource/llm-applications-cybersecurity-and-governance-checklist-english/) - 13-area checklist for security leaders deploying LLMs.

### Threat Models, Taxonomies & Government Guidance

- [**MITRE ATLAS**](https://atlas.mitre.org/) - Adversarial Threat Landscape for AI Systems: ATT&CK-style matrix of real-world ML attack tactics and techniques.
- [**CSA MAESTRO – Agentic AI Threat Modeling**](https://cloudsecurityalliance.org/blog/2025/02/06/agentic-ai-threat-modeling-framework-maestro) - Seven-layer threat-modeling framework purpose-built for multi-agent systems.
- [**CISA & NCSC Joint Guidelines for Secure AI System Development**](https://www.cisa.gov/news-events/alerts/2023/11/26/cisa-and-uk-ncsc-unveil-joint-guidelines-secure-ai-system-development) - Joint US/UK + 23-country secure-by-design guidance.
- [**Google Secure AI Framework (SAIF)**](https://safety.google/cybersecurity-advancements/saif/) - Six-element conceptual framework for securing AI systems.

### Red-Teaming & Adversarial Testing

- [**NVIDIA Garak**](https://github.com/NVIDIA/garak) - Open-source LLM vulnerability scanner with probes for jailbreaks, prompt injection, and data leakage. Python CLI — can target PHP-hosted LLM endpoints.
- [**Promptfoo Red Team**](https://www.promptfoo.dev/docs/red-team/) - Plugin-based adversarial testing framework; CLI-runnable from PHP CI/CD pipelines.
- [**HackAPrompt**](https://www.hackaprompt.com/) - Largest open prompt-injection competition dataset.
- [**Lakera Gandalf**](https://gandalf.lakera.ai/) - Public prompt-injection challenge; corpus seeds Lakera Guard detectors.

### Runtime Guardrails (PHP-accessible)

- [**AWS Bedrock Guardrails**](https://docs.aws.amazon.com/bedrock/latest/userguide/guardrails.html) - Content filtering, PII redaction, and grounding checks accessible via `aws/aws-sdk-php` (`BedrockRuntimeClient`). **The most practical PHP-native guardrails path** for apps on Bedrock.
- [**Lakera Guard**](https://www.lakera.ai/lakera-guard) - Runtime REST API for prompt-injection, jailbreak, PII, and agent tool-call policy enforcement; consumable from any PHP HTTP client.
- [**OpenAI Moderation API**](https://platform.openai.com/docs/guides/moderation) - Accessible via `openai-php/client`; provides content safety classification at zero cost.
- [**Microsoft Presidio**](https://microsoft.github.io/presidio/) - PII detection and anonymization (Python core); deployable as a sidecar service callable from PHP apps via REST.
- [**NVIDIA NeMo Guardrails**](https://github.com/NVIDIA/NeMo-Guardrails) - Programmable guardrails (Colang DSL); Python runtime, callable from PHP apps via API.
- *Gap*: No PHP-native prompt-injection detection or AI output validation library currently exists on Packagist. **Contributions welcome.**

---

## Contributing

Contributions are welcome! Please read the [contribution guidelines](CONTRIBUTING.md) first.

## License
[![CC BY-SA 4.0][cc-by-sa-image]][cc-by-sa]

This work is licensed under a [Creative Commons Attribution-ShareAlike 4.0 International License][cc-by-sa].

[cc-by-sa]: http://creativecommons.org/licenses/by-sa/4.0/
[cc-by-sa-image]: https://licensebuttons.net/l/by-sa/4.0/88x31.png

[https://github.com/andreibesleaga/awesome-ai-php](https://github.com/andreibesleaga/awesome-ai-php)
