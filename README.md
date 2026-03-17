# 🌱 AgroEdge-AI

[![Agent Ready](https://img.shields.io/badge/Agent--Ready-AGENTS.md-blue)](AGENTS.md)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

> **Context-aware multiagent architecture (LangGraph + MCP) for safe decision support in tropical agriculture.**
>
> *Arquitetura multiagente (LangGraph + MCP) ciente de contexto para suporte seguro à decisão na agricultura tropical.*

AgroEdge-AI is a research-driven open-source project designed to solve the critical "environmental context gap" in agricultural LLMs. By combining static agronomic knowledge (RAG) with dynamic real-time telemetry, this system introduces **Environmental Guardrails**—ensuring that AI-generated agricultural recommendations are strictly validated against real-world physical conditions before execution.

## 🎯 The Problem & Our Solution

Generic LLMs and standard Retrieval-Augmented Generation (RAG) systems fail in agriculture because they treat the physical world as static. Recommending chemical fertilizers based on a textbook is dangerous if a storm is approaching the farm.

AgroEdge-AI intercepts these theoretical recommendations and cross-references them with real-time microclimate data using the **Model Context Protocol (MCP)**. If environmental conditions prohibit the action, the system autonomously overrides the recommendation, preventing resource waste and environmental liabilities.

## 🏗️ Architecture & Tech Stack

The architecture is built for **Edge AI**, prioritizing low-latency inference on resource-constrained hardware typical of rural environments.

  * **Orchestration:** LangGraph 1.0 (Stateful Multiagent Graph)
  * **Tool Integration:** Model Context Protocol (MCP)
  * **Core SLM:** Meta Llama 3.1 8B Instruct / Qwen3-8B
  * **Vector Database:** ChromaDB (Local execution)

## 🌏 Sino-Brazilian Strategic Alignment

This project is strategically aligned with the global transition towards sustainable family farming and decentralized smart agriculture. The architecture serves as a foundational logic layer that complements the hardware and machinery initiatives spearheaded by the joint laboratory for Artificial Intelligence and family farming, established by Brazil's National Institute of the Semi-Arid (INSA) and the China Agricultural University (CAU). By focusing on low-cost edge computing and input optimization, AgroEdge-AI addresses the mutual goals of food security, climate resilience, and scalable digital management.

## 🚀 Quick Start (MVP)

### Prerequisites

  * Python 3.11+
  * `uv` package manager (recommended for fast dependency resolution)
  * OpenWeather API Key

### Installation

1.  Clone the repository:bash
    git clone [https://github.com/rafaeumesmo/AgroEdge-AI](https://github.com/rafaeumesmo/AgroEdge-AI)
    cd AgroEdge-AI

<!-- end list -->
https://github.com/rafaeumesmo/AgroEdge-AI
````

2. Set up the environment and install dependencies:
```bash
uv venv
source.venv/bin/activate
uv pip install -r requirements.txt
````

3.  Configure your environment variables:

<!-- end list -->

```bash
cp configs/.env.example configs/.env
# Add your API keys to configs/.env
```

4.  Run the Streamlit Demo:

<!-- end list -->

```bash
streamlit run src/app.py
```

## 🤖 Agentic Web Ready

This repository is optimized for autonomous AI coding agents. We maintain an `AGENTS.md` file in the root directory that provides specific context, coding standards, and architectural constraints for agents like Claude Code, Cursor, or Aider interacting with this codebase.

## 📊 Evaluation & Testing

AgroEdge-AI utilizes synthetic adversarial testing to validate its environmental guardrails. The system is evaluated not just on conversational accuracy, but on **Goal Success** and **Tool Selection Accuracy** when faced with conflicting agronomic and climatic variables.

To run the test suite:

```bash
pytest tests/
```

## 🤝 Contributing

We welcome contributions from researchers and developers focusing on Precision Agriculture, Agentic AI, and Cyber-Physical Systems. Please read our contribution guidelines before submitting a Pull Request.

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

```
```
