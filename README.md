# Awesome AI PHP [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

A curated list of **PHP** libraries, SDKs, frameworks, and software for **Artificial Intelligence**, **LLMs**, **Machine Learning**, and **Agentic AI**.

> PHP is evolving. With modern asynchronous frameworks and robust type systems, it's becoming a solid choice for orchestrating AI agents and integrating LLMs into business logic.

## Contents

- [Large Language Models (LLMs)](#large-language-models-llms)
- [Framework Integrations](#framework-integrations)
- [Agentic AI & Frameworks](#agentic-ai--frameworks)
- [AI Protocols (MCP, A2A)](#ai-protocols-mcp-a2a)
- [Machine Learning](#machine-learning)
- [Vector Databases](#vector-databases)
- [Natural Language Processing (NLP)](#natural-language-processing-nlp)
- [Computer Vision](#computer-vision)
- [Voice & Audio](#voice--audio)
- [Infrastructure & Cloud AI](#infrastructure--cloud-ai)
- [Spotlight: 2026 & Trending](#spotlight-2026--trending)
- [Learning Resources](#learning-resources)

---

## Large Language Models (LLMs)
*Clients and SDKs for popular LLM providers.*

- [openai-php/client](https://github.com/openai-php/client) - A supercharged community-maintained PHP client for the OpenAI API.
- [lanos/anthropic](https://github.com/Lanos/anthropic) - A PHP client for the Anthropic Claude API.
- [gemini-api-php/client](https://github.com/gemini-api-php/client) - PHP Client for Gemini AI API.
- [modelflow-ai/mistral](https://github.com/modelflow-ai/mistral) - A PHP API Client for Mistral AI.
- [ardagnsrn/ollama-php](https://github.com/ArdaGnsrn/ollama-php) - A PHP library for Ollama, enabling local LLM execution.
- [koco/anthropic](https://github.com/koco-php/anthropic) - Another robust Anthropic client.
- [deepseek-php/client](https://github.com/deepseek-php/client) - Community client for the trending DeepSeek LLM.

## Framework Integrations
*AI tools tailored for specific PHP frameworks.*

### Laravel
- [laravel/ai](https://github.com/laravel/ai) - The **Official** Laravel AI SDK. Provides a unified API for interacting with various AI providers (OpenAI, Anthropic, Gemini, etc.) and building AI-powered applications.
- [echolabsdev/prism](https://prism.echolabs.dev/) - A unified LLM package for Laravel that abstracts provider differences (OpenAI, Anthropic, Ollama).
- [openai-php/laravel](https://github.com/openai-php/laravel) - The official-ish Laravel wrapper for the OpenAI PHP client.
- [gemini-api-php/laravel](https://github.com/gemini-api-php/laravel) - Laravel integration for Gemini AI.
- [neuron-ai/neuron-laravel](https://neuron-ai.dev/) - Laravel adapter for the Neuron AI agentic framework.
- [laravel-boost](https://github.com/mpociot/laravel-boost) - An MCP Server implementation that gives AI agents access to your Laravel app's context.

### Symfony
- [symfony/ai](https://github.com/symfony/ai) - **Official** Symfony components for building AI-enabled applications (Experimental).
- [php-llm/llm-chain-bundle](https://github.com/php-llm/llm-chain-bundle) - Symfony bundle for the LLPhant/Chain ecosystem.

### Yii & CodeIgniter
- [ldkafka/yii2-google-gemini](https://github.com/ldkafka/yii2-google-gemini) - Gemini AI integration for Yii2.
- *General Note*: Most generic PHP clients (like `openai-php/client`) work seamlessly in any PHP framework.

## Agentic AI & Frameworks
*Frameworks for building autonomous agents, reasoning engines, and complex AI applications.*

- [Neuron AI](https://neuron-ai.dev/) - **Best-in-class** full-featured agentic framework for PHP. Designed to build autonomous agents that can plan, use tools, search data, and interact with various LLM providers (OpenAI, Anthropic, Ollama, etc.).
- [Utopia Agents](https://github.com/utopia-php/agents) - A lightweight, framework-agnostic library for creating and orchestrating AI agents. Supports multiple providers and is optimized for performance.
- [LLPhant](https://github.com/theodorejb/LLPhant) - A comprehensive Generative AI Framework for PHP, heavily inspired by **LangChain**. Supports OpenAI, Anthropic, Ollama, and vector stores.
- [LLM Agents PHP](https://github.com/rabbotio/llm-agents-php) - A library specifically designed for creating and managing LLM-based autonomous agents with memory and tool capabilities.
- [Resonance](https://github.com/distantmagic/resonance) - An asynchronous PHP framework optimized for IO-intensive tasks, widely used for serving ML models and building high-concurrency agent backends.
- [Phullstack/Agents](https://github.com/phullstack/agents) - Minimalist agent implementation for PHP.

### Agentic Patterns
- **RAG (Retrieval Augmented Generation)**: Most frameworks above (Neuron, LLPhant) support RAG out of the box.
- **Tool Use**: Standardized ways for PHP scripts to expose functions to LLMs (via JSON schemas).
- **Planner/Reasoning**: Implementing "Reason-Act" (ReAct) loops in PHP to allow agents to solve multi-step problems.

## AI Protocols (MCP, A2A)
*Implementations of modern AI communication protocols.*

### Model Context Protocol (MCP)
*Standard for connecting AI models to external data and tools.*
- [php-mcp/sdk](https://github.com/php-mcp/sdk) - **Official** PHP SDK for building MCP servers, utilized by the PHP Foundation.
- [logiscape/mcp-sdk-php](https://github.com/Logiscape/mcp-sdk-php) - Complete SDK for building both MCP **Clients** and **Servers**.
- [swisnl/mcp-client](https://github.com/swisnl/mcp-client) - An asynchronous PHP client for the Model Context Protocol.
- [james2037/mcp-php-server](https://github.com/james2037/mcp-php-server) - A focused MCP Server implementation.
- [lobehub/php-mcp-server](https://github.com/lobehub/php-mcp-server) - Robust MCP server implementation supporting PHP 8 attributes.

### Agent-to-Agent (A2A) Protocol
*Protocol for seamless communication between autonomous agents.*
- [andreibesleaga/a2a-php](https://github.com/andreibesleaga/a2a-php) - A comprehensive PHP implementation of the A2A protocol.
- [aurimasbutkus/a2a-php](https://github.com/aurimasbutkus/a2a-php) - Framework-agnostic A2A protocol implementation.

## Machine Learning
*Core libraries for training and running ML models in PHP.*

- [Rubix ML](https://rubixml.com/) - A high-level machine learning and deep learning library for PHP. Supports nearly every type of ML task from classification/regression to clustering and anomaly detection.
- [PHP-ML](https://github.com/php-ai/php-ml) - A library for machine learning in PHP. Include algorithms, cross-validation, neural network, preprocessing, feature extraction and much more.

## Vector Databases
*PHP clients for vector stores, essential for RAG (Retrieval-Augmented Generation).*

- [hkulekci/qdrant-php](https://github.com/hkulekci/qdrant-php) - PHP Client for Qdrant Vector Database.
- [probots-io/pinecone-php](https://github.com/probots-io/pinecone-php) - A PHP client for Pinecone.
- [timkley/weaviate-php](https://github.com/timkley/weaviate-php) - PHP Client for Weaviate.
- [codewithkyrian/chromadb-php](https://github.com/CodeWithKyrian/chromadb-php) - ChromaDB client for PHP.

## Natural Language Processing (NLP)
*Tools for processing and analyzing text.*

- [Text Analysis](https://github.com/yooper/php-text-analysis) - A library for performing information retrieval (IR) and NLP tasks.
- [patrickschur/language-detection](https://github.com/patrickschur/language-detection) - A language detection library for PHP.
- [yooper/php-text-analysis](https://github.com/yooper/php-text-analysis) - Analysis tool for texts.

## Computer Vision
*Image processing and vision capabilities.*

- [Google Cloud Vision](https://github.com/googleapis/google-cloud-php-vision) - Google Cloud Vision API client for PHP.
- [Azure Computer Vision](https://github.com/microsoft/azure-docs) - Integration usually handled via generic HTTP clients/SDKs, but specific wrappers exist.

## Voice & Audio
*Speech-to-Text (STT) and Text-to-Speech (TTS).*

- [Laravis](https://github.com/Laravis) - (Check for specific audio packages)
- [openai-php/client](https://github.com/openai-php/client) - Supports OpenAI's Whisper model for transcription.

## Infrastructure & Cloud AI
*SDKs and tools for deploying AI on major cloud providers and specialized infrastructure.*

### AWS (Amazon Web Services)
- [aws/aws-sdk-php](https://github.com/aws/aws-sdk-php) - Official AWS SDK for PHP. Supports **Amazon Bedrock** (Serverless LLMs) and **Amazon SageMaker**.
- [echolabsdev/prism-bedrock](https://github.com/echolabsdev/prism-bedrock) - Bedrock provider for the Prism Laravel package.

### Google Cloud Platform (GCP)
- [google/cloud-vertex-ai](https://github.com/googleapis/google-cloud-php-vertex-ai) - Official PHP client for Google Cloud Vertex AI.
- [google-gemini-php/client](https://github.com/google-gemini-php/client) - Community client for Gemini AI.

### Azure (Microsoft)
- [openai-php/client](https://github.com/openai-php/client) - The recommended client for connecting to **Azure OpenAI**.
- [kvaksrud/laravel-azure-cognitive-services-api](https://github.com/Kvaksrud/laravel-azure-cognitive-services-api) - Wrapper for Azure Cognitive Services.

### Specialized AI Infrastructure
- [mateffy/huggingface](https://github.com/mateffy/huggingface) - Unofficial PHP SDK for the **Hugging Face** Inference API.
- [kambo-1st/huggingface-php](https://github.com/kambo-1st/huggingface-php) - Comprehensive Hugging Face API client.
- [sabinomasala/replicate-php](https://github.com/SabatinoMasala/replicate-php) - PHP client for **Replicate** to run open-source models (Llama 3, Stable Diffusion) via API.
- [benbjurstrom/replicate-php](https://github.com/benbjurstrom/replicate-php) - Another robust Replicate client built on Saloon.

## Spotlight: 2026 & Trending
*New and rapidly growing projects shaping the PHP AI landscape in 2026.*

- **[Symfony AI](https://github.com/symfony/ai)**: Now **stable (v0.2.0)** as of Jan 2026. The official entry of Symfony into the AI space marks a major maturity point for the ecosystem.
- **[LLPhant](https://github.com/theodorejb/LLPhant)**: continues to be the "LangChain for PHP", bridging the gap for complex chains and RAG.
- **[Prism](https://prism.echolabs.dev/)**: Rapidly becoming the standard abstraction layer for Laravel developers to switch between LLMs easily.

## Learning Resources
*High-quality tutorials, courses, and guides for building AI with PHP.*

### Courses
- [AI Machine Learning Complete Course: for PHP & Python Devs](https://www.udemy.com/course/machine-learning-artificial-intelligence-in-php/) - (Udemy) A comprehensive course covering AI fundamentals, Machine Learning types, and building AI agents, specifically tailored for PHP developers. Updated late 2025.

### Tutorials & Articles
- [Building my first AI agent with Neuron AI and Ollama](https://dev.to/neuron-ai/building-my-first-ai-agent-with-neuron-ai-and-ollama-2b5e) - Step-by-step guide to running local agents.
- [How to create AI Agents in PHP with Neuron AI framework](https://www.youtube.com/watch?v=...) - Video tutorial on practical agent creation.
- [The Ultimate Guide to PHP AI APIs Integration in 2026](https://phptutorialpoints.in/ultimate-guide-php-ai-apis-integration-2026-chatgpt-gemini-claude/) - Deep dive into connecting PHP with major AI providers.
- [Building LLM Applications with PHP](https://bacancytechnology.com/blog/build-llm-application-with-php) - Guide on integrating LLMs into PHP apps.

### Community & Documentation
- [Neuron AI Documentation](https://neuron-ai.dev/docs) - Excellent docs for the leading PHP agent framework.
- [LLPhant Documentation](https://llphant.io/) - Guides for the "LangChain of PHP".
- [PHP Foundation - AI Discussions](https://thephp.foundation/) - Follow for official announcements regarding the PHP MCP SDK.

## Contributing

Contributions are welcome! Please read the [contribution guidelines](CONTRIBUTING.md) first.

## License
[![CC BY-SA 4.0][cc-by-sa-image]][cc-by-sa]

This work is licensed under a [Creative Commons Attribution-ShareAlike 4.0 International License][cc-by-sa].

[cc-by-sa]: http://creativecommons.org/licenses/by-sa/4.0/
[cc-by-sa-image]: https://licensebuttons.net/l/by-sa/4.0/88x31.png
