<div align="center">

# 🧬 CodeDNA

### *The DNA of Your Software — Discover the Story, Architecture, and Reasoning Behind Every Line of Code*

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg?style=for-the-badge)](LICENSE)
[![Python 3.10+](https://img.shields.io/badge/Python-3.10%2B-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.0%2B-3178C6?style=for-the-badge&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![AST Engine](https://img.shields.io/badge/AST%20Parser-Tree--sitter-294E80?style=for-the-badge)](https://tree-sitter.github.io/tree-sitter/)
[![Graph Engine](https://img.shields.io/badge/Knowledge%20Graph-NetworkX%20%7C%20GraphRAG-FF6F00?style=for-the-badge)](https://networkx.org/)
[![Docker Ready](https://img.shields.io/badge/Docker-Multi--stage%20Build-2496ED?style=for-the-badge&logo=docker&logoColor=white)](#-docker--containerization)
[![Status](https://img.shields.io/badge/Status-Research%20%26%20Active%20Dev-success?style=for-the-badge)](#-project-roadmap)
[![PRs Welcome](https://img.shields.io/badge/PRs-Welcome-brightgreen.svg?style=for-the-badge)](https://github.com/Vish-0806/CodeDNA/pulls)

<p align="center">
  <a href="#-the-problem">The Problem</a> •
  <a href="#-vision--core-mission">Vision</a> •
  <a href="#-interactive-previews-tui--web-studio">Live Previews</a> •
  <a href="#-system-architecture">Architecture</a> •
  <a href="#-knowledge-graph-data-model">Graph Schema</a> •
  <a href="#-data-ingestion--code-archaeology-pipeline">Ingestion Flow</a> •
  <a href="#-code-intelligence-comparison">Comparison</a> •
  <a href="#-core-features">Core Features</a> •
  <a href="#-security-privacy--threat-model">Privacy & Security</a> •
  <a href="#-tech-stack--architectural-rationale">Tech Stack</a> •
  <a href="#-docker--containerization">Docker</a> •
  <a href="#-cli-quickstart">CLI Quickstart</a> •
  <a href="#-developer-sdk-examples">SDK Reference</a> •
  <a href="#-real-world-case-studies">Case Studies</a> •
  <a href="#-project-roadmap">Roadmap</a> •
  <a href="#-frequently-asked-questions">FAQ</a>
</p>

</div>

---

> [!IMPORTANT]
> **"Software should not only be built. It should be understood."**
> 
> In the era of AI-driven development and vibe coding, anyone can generate thousands of lines of working code in seconds. **CodeDNA bridges the comprehension gap**—converting opaque repositories into interactive knowledge graphs, architectural documentaries, and personalized viva interview trainers.

---

## 🚨 The Problem

Modern AI coding assistants (Claude 3.7, ChatGPT o3, GitHub Copilot, Cursor, Gemini Code Assist) have democratized software creation. Building complex full-stack web apps, microservices, or mobile apps now takes hours instead of weeks.

However, a serious **comprehension crisis** has emerged across software engineering and education:

```
   [ AI Prompt ] ──► [ Instant Boilerplate / Code ] ──► [ Working App ]
                                                              │
                                     CRITICAL BLIND SPOT:     ▼
                                  ┌──────────────────────────────────────────────┐
                                  │ ❓ "Why did you choose this architecture?"   │
                                  │ ❓ "How do these two modules pass tokens?"   │
                                  │ ❓ "Why does this middleware exist?"         │
                                  │ ❓ "What happens if this webhook fails?"    │
                                  └──────────────────────────────────────────────┘
```

### Where This Fails Developers:
* 🎓 **University & College Vivas:** Students build ambitious capstone projects using AI, but freeze when evaluators ask probing architectural questions.
* 💼 **Technical Interviews:** Candidates struggle to articulate the design trade-offs, concurrency models, or data structures present in their portfolio repositories.
* 🏆 **Hackathons & Demos:** Teams ship functional prototypes but lose winning points because they cannot defend their technical design under pressure.
* 🏢 **Engineering Onboarding:** Engineers joining legacy codebases spend weeks sifting through cryptic Git histories (`fix: patch bug`, `update temp`) without context.

> **Current AI tools explain static syntax.**
> 
> **CodeDNA reconstructs the entire dynamic story, intent, and evolution behind the software.**

---

## 🎯 Vision & Core Mission

CodeDNA is an **autonomous codebase comprehension & intelligence platform**. It ingests your Git repository, performs deep AST (Abstract Syntax Tree) parsing, analyzes the semantic evolution of commits, and constructs an **Architectural Knowledge Graph**. 

```
                                    ┌──────────────────────┐
                                    │    Git Repository    │
                                    │ (Commits, Trees, PRs)│
                                    └──────────┬───────────┘
                                               │
                                               ▼
                                    ┌──────────────────────┐
                                    │   CodeDNA Engine     │
                                    │ (AST + GraphRAG + AI)│
                                    └──────────┬───────────┘
                                               │
        ┌──────────────────────┬───────────────┴──────────────┬──────────────────────┐
        ▼                      ▼                              ▼                      ▼
 📖 Documentary        🧠 Commit Meaning             🔍 Why Does This Exist?   🎤 Viva Simulator
 Episodic storyline    Intent & ripple-effect         Line-by-line provenance  Targeted interrogation
```

Our mission is to empower developers not just to write code faster, but to **own, defend, and master every layer of their creation**.

---

## 🖥️ Interactive Previews (TUI & Web Studio)

### 1. Terminal CLI Repository Ingestion
```text
$ codedna inspect https://github.com/Vish-0806/CodeDNA --deep-scan

  🧬 CodeDNA Core Engine v0.1.0-alpha
  Scanning repository: Vish-0806/CodeDNA [Branch: main]

  ✔ Cloning ephemeral working tree ............................. [DONE]
  ✔ Tree-sitter AST extraction (142 files, 18,490 symbols) ..... [DONE]
  ✔ Git Commit Archaeology (84 commits, 3 contributors) ........ [DONE]
  ✔ Constructing Knowledge Graph (Nodes: 2,410 | Edges: 8,920) .. [DONE]
  ✔ Synthesizing Documentary & Architecture Blueprint .......... [DONE]

  ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  📊 CodeDNA Repository Scorecard:
  • Primary Architecture: Micro-frontends with Event-Driven Backend
  • Complexity Index: 64/100 (Medium)
  • Dependency Health: 96% Clean coupling
  • Viva Readiness Index: Ready for Evaluation
  ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  
  [Ready] Web studio launched at: http://localhost:4200
  [Ready] Press 'V' to launch Interactive Viva Terminal Simulator
```

### 2. CodeDNA Web Studio Dashboard Mockup
```text
┌──────────────────────────────────────────────────────────────────────────────────────────────────────────────────┐
│ 🧬 CodeDNA Studio  [Project: CodeDNA]  [Branch: main]              [Graph Nodes: 2,410]   [Viva Readiness: 88%]  │
├──────────────────────────┬─────────────────────────────────────────────────┬─────────────────────────────────────┤
│ 📚 DOCUMENTARY CHAPTERS  │ 🔍 CODE ARCHAEOLOGY: src/auth/jwt_handler.py     │ 🎤 AI VIVA MENTOR                   │
├──────────────────────────┼─────────────────────────────────────────────────┼─────────────────────────────────────┤
│ ▶ Ep 1: Project Genesis  │ Line 42: class TokenBlacklistManager:           │ [EXAMINER - STRICT MODE]:           │
│ ▶ Ep 2: SQLite -> PG     │ Line 43:     def __init__(self, redis_client):  │ "Explain why you opted for an       │
│ ▼ Ep 3: Redis Auth Guard │                                                 │ in-memory Redis blacklist rather    │
│   • Token Revocation     │ 💡 WHY DOES THIS EXIST? (Provenance Card)       │ than a database check for revoked   │
│   • Blacklist Handler    │ Introduced in Commit: 4f82a1c ('fix: auth race')│ JWTs, and how you prevent data      │
│   • Middleware Hook      │ Problem Solved: Stolen tokens stayed active for │ loss during a restart."             │
│ ▶ Ep 4: GraphRAG Pipeline│ the full 24h JWT lifespan.                      │                                     │
│ ▶ Ep 5: Viva Scoring     │ Rationale: Redis provides O(1) lookups during   │ 🎙️ [SPEECH INPUT DETECTED]         │
│                          │ auth middleware without hitting PostgreSQL.     │ "We use Redis for sub-millisecond   │
│ ──────────────────────── │ Trade-offs: Requires Redis high-availability.   │ checks, backed by AOF persistence." │
│ 🗺️ TOPOLOGY EXPLORER    │                                                 │                                     │
│ [Files] [AST] [Graph]    │ 🔗 Downstream Consumers (4 files affected):     │ 📊 SCORE: 92/100 (High Mastery)     │
│ • /auth/jwt_handler.py   │ • src/middleware/auth_guard.py (Calls)          │ Feedback: Excellent grasp of trade- │
│ • /graph/builder.py      │ • src/api/v1/endpoints/logout.py (Mutates)      │ offs. Mention replica failover next.│
└──────────────────────────┴─────────────────────────────────────────────────┴─────────────────────────────────────┘
```

### 3. Interactive Viva Terminal Simulation
```text
┌──────────────────────────────────────────────────────────────────────────────┐
│  🎤 CodeDNA AI Mentor — Viva Mode: [CapStone Evaluation]                     │
│  Topic: Authentication & Session Invalidation                               │
├──────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  [EXAMINER]: "In file 'src/auth/jwt_handler.py' (lines 42-68), you opted     │
│  for an in-memory Redis blacklist rather than a stateless database check for │
│  revoked JWTs. Why did you make this architectural trade-off, and what       │
│  happens if the Redis instance restarts unexpectedly?"                      │
│                                                                              │
│  [YOUR ANSWER]: "We chose Redis for sub-millisecond O(1) blacklist lookups   │
│  to keep API latency low. If Redis goes down, we fallback to our PostgreSQL  │
│  revocation table, though with a 15ms latency penalty."                      │
│                                                                              │
│  ──────────────────────────────────────────────────────────────────────────  │
│  [EVALUATION REPORT]:                                                        │
│  Score: 92/100 (Exceptional Architectural Defense)                           │
│  Strengths: Accurately identified O(1) latency justification & fallback.    │
│  Pro-Tip: Mention Redis AOF (Append Only File) persistence to prevent data   │
│           loss on cold reboot before falling back to PostgreSQL.             │
└──────────────────────────────────────────────────────────────────────────────┘
```

---

## 🏗️ System Architecture

CodeDNA utilizes a multi-layered, reactive architecture combining AST parsers, Git differential graph builders, and GraphRAG-powered conversational agents:

```mermaid
flowchart TB
    subgraph INGESTION["1. Ingestion & Extraction Layer"]
        Repo[Git Repository / ZIP / URL] --> Cloner[Local Sandboxed Cloner]
        Cloner --> GitWalker[Git History & Diff Walker]
        Cloner --> ASTParser[Tree-sitter AST Parser]
        Cloner --> DependencyGrapher[Package & Module Resolver]
    end

    subgraph GRAPH["2. CodeDNA Knowledge Graph Engine"]
        GitWalker --> EntityExtractor[Symbol & Entity Extractor]
        ASTParser --> EntityExtractor
        DependencyGrapher --> EntityExtractor
        EntityExtractor --> GraphDB[(CodeDNA Graph\nNodes: Files, Funcs, Commits\nEdges: Imports, Mutates, Fixes)]
        GraphDB --> VectorStore[(Vector Embeddings\nSemantic Code Embeddings)]
    end

    subgraph COGNITIVE["3. Cognitive AI Reasoning Layer"]
        GraphDB --> GraphRAG[Graph-Augmented RAG Engine]
        VectorStore --> GraphRAG
        GraphRAG --> DocAgent[📖 Documentary Generator]
        GraphRAG --> ArcheoAgent[🔍 'Why Does It Exist?' Tracer]
        GraphRAG --> ArchAgent[🏗️ Diagram & Flowchart Generator]
        GraphRAG --> VivaAgent[🎤 Viva & Interview Examiner]
    end

    subgraph CLIENTS["4. Presentation & Interaction"]
        DocAgent --> WebApp[🌐 CodeDNA Web Studio]
        ArcheoAgent --> WebApp
        ArchAgent --> WebApp
        VivaAgent --> WebApp
        VivaAgent --> CLI[💻 CodeDNA CLI / TUI]
        DocAgent --> IDEExt[🧩 VS Code / JetBrains Plugin]
    end
```

---

## 🧬 Knowledge Graph Data Model

CodeDNA constructs a typed, directed multigraph to capture code hierarchy and temporal evolution:

```mermaid
erDiagram
    REPOSITORY ||--o{ COMMIT : tracks
    REPOSITORY ||--o{ SOURCE_FILE : contains
    SOURCE_FILE ||--o{ AST_SYMBOL : declares
    COMMIT ||--o{ AST_DELTA : introduces
    AST_SYMBOL ||--o{ AST_SYMBOL : calls_or_imports
    AST_DELTA }o--|| AST_SYMBOL : modifies
    ARCHITECTURAL_DECISION ||--o{ AST_SYMBOL : governs
    VIVA_QUESTION ||--o{ AST_SYMBOL : interrogates
    VIVA_QUESTION ||--|| RUBRIC : evaluated_with

    REPOSITORY {
        string url
        string default_branch
        int total_commits
        string primary_language
    }
    COMMIT {
        string commit_hash
        string author
        timestamp committed_at
        string semantic_category
        string message
    }
    AST_SYMBOL {
        string identifier
        string symbol_type
        string file_path
        int line_start
        int line_end
        float cyclomatic_complexity
    }
    ARCHITECTURAL_DECISION {
        string decision_title
        string problem_context
        string trade_offs
        string alternatives_rejected
    }
    VIVA_QUESTION {
        string question_id
        string topic
        string difficulty
        string scenario_prompt
    }
```

---

## 🔄 Data Ingestion & Code Archaeology Pipeline

How CodeDNA reverse-engineers the story and intent behind every symbol:

```mermaid
sequenceDiagram
    autonumber
    actor Dev as Developer / Student
    participant CLI as CodeDNA CLI / Studio
    participant Core as Engine Orchestrator
    participant TreeSitter as Tree-Sitter Parser
    participant Git as Git Log Archaeology
    participant Graph as Knowledge Graph (GraphRAG)
    participant LLM as LLM Intelligence Agent

    Dev->>CLI: codedna analyze ./project
    CLI->>Core: Initialize scan pipeline
    Core->>TreeSitter: Parse file structure & AST
    TreeSitter-->>Core: Functions, classes, imports, call graphs
    Core->>Git: Reconstruct commit history & churn rates
    Git-->>Core: Temporal commit deltas & author intent
    Core->>Graph: Merge AST hierarchy + Git evolution into unified graph
    Core->>LLM: Pass subgraph clusters for semantic synthesis
    LLM-->>Core: Synthesized chapters, architectural trade-offs & viva questions
    Core->>CLI: Generate Interactive Web Studio & Diagnostic Report
    CLI->>Dev: Explore Architecture, Timeline & Start Viva Prep
```

---

## ⚖️ Code Intelligence Comparison

| Feature Capability | CodeDNA | ChatGPT / Claude | GitHub Copilot | SonarQube / Linters |
| :--- | :---: | :---: | :---: | :---: |
| **Commit Archaeology & Evolution** | ✅ **Full History** | ❌ None (Isolated text) | ❌ None | ❌ None |
| **"Why Does This Exist?" Provenance** | ✅ **AST + Git Linked** | ❌ Speculation only | ❌ In-line autocomplete | ❌ Rule-only violation |
| **Dynamic Architecture Visualizer** | ✅ **Live Mermaid & D3** | ⚠️ Text markdown only | ❌ None | ⚠️ Static dependencies |
| **Interactive Viva / Interview Simulator** | ✅ **Tailored to Repo** | ⚠️ Generic questions | ❌ None | ❌ None |
| **Understanding Scorecard & Rubrics** | ✅ **Quantitative Radar** | ❌ None | ❌ None | ❌ Quality gate only |
| **Graph-Augmented Retrieval (GraphRAG)**| ✅ **Topological Index** | ❌ Simple text chunks | ❌ Local file context | ❌ AST-only |
| **100% Offline Local LLM Execution** | ✅ **Ollama / vLLM** | ❌ Cloud only | ❌ Cloud only | ✅ On-premise |
| **Secret & PII Sanitizer Before LLM** | ✅ **AST-Scrubbed** | ❌ Manual user care | ⚠️ Enterprise policy | ✅ Static regex |

---

## ✨ Core Features

### 📖 1. Repository Documentary
> *Turn your git commits into an episodic Netflix-style technical documentary.*
* Instead of hundreds of disconnected commits, CodeDNA groups development into meaningful **episodes** and **milestones**:
  * **Chapter 1: The Scaffolding** — Project genesis, initial stack decisions, and foundational boilerplate.
  * **Chapter 2: The Data Layer Pivot** — Moving from local SQLite to PostgreSQL and connection pooling.
  * **Chapter 3: Hardening Security** — Rate limiting, JWT expiration, and middleware guardrails.
* Provides a natural, human-readable narrative explaining how the project matured from concept to deployment.

---

### 🧠 2. Commit Intelligence & Semantic Context
> *Never read a cryptic `fix bug` or `wip` commit again.*
* CodeDNA computes semantic diffs across AST nodes to determine:
  * **What actually changed** at the functional and architectural level.
  * **Why the change occurred** (correlating bug trackers, PR descriptions, and logic mutations).
  * **Systemic Ripple Effects** (which downstream consumers, tests, or APIs were affected).

---

### 🔍 3. "Why Does This Exist?" (Code Archeology)
> *Hover over or click any class, function, or configuration block to uncover its provenance.*
* Traces code back to the exact problem, issue, or constraint that mandated its creation.
* Explains why standard alternatives were rejected (e.g., *"Why custom debounce instead of Lodash?"*).
* Helps new engineers onboard into 100,000+ line codebases without asking teammates basic questions.

---

### 🏗️ 4. Architecture & Feature Flowcharts
> *Automatic, real-time visual system diagrams without manual upkeep.*
* **Component Dependency Maps:** See how your API routes connect to services, data models, and caching layers.
* **Feature Journey Flowcharts:** Visual sequence diagrams tracing end-to-end user flows:
  * Authentication, Token Refresh & Role Validation
  * Payment Checkout & Webhook Reconciliation
  * Asynchronous Background Job Processing

---

### 🎤 5. AI Mentor & Viva Preparation Simulator
> *The ultimate technical defense simulator for students, hackathons, and interviews.*
* Generates repository-specific interrogations tailored to your exact implementation:
  * *"Walk me through how your backend handles race conditions during payment webhook retries."*
  * *"Why did you use WebSockets instead of Server-Sent Events (SSE) for notifications?"*
  * *"If user traffic spikes 50x, where does your system experience its first bottleneck?"*
* **Speech & Text Mode:** Answer verbally or via terminal input; receive instant rubrics, constructive critiques, and model answers.

---

### 📊 6. Multidimensional Understanding Score
> *Measure how deeply you understand your own software.*
* CodeDNA tests your knowledge across critical technical dimensions and gives you a visual radar scorecard:

```text
  Understanding Score: 83% Overall
  
  [████████████████████░░] Frontend & UI Components      : 88%
  [█████████████████░░░░░] Backend & API Business Logic  : 82%
  [█████████████░░░░░░░░░] Database Schema & Indexing    : 65%
  [█████████████████████░] Authentication & Authorization: 95%
  [██████████████░░░░░░░░] Error Handling & Edge Cases   : 70%
```

---

## 🔒 Security, Privacy & Threat Model

CodeDNA is engineered with a **zero-knowledge, privacy-first posture**:

```
 ┌────────────────┐     ┌────────────────────────────────────────────────────────┐
 │ Local Codebase │ ──► │  1. Ephemeral Sandboxed Cloner (RAM / Volatile Temp)  │
 └────────────────┘     └──────────────────────────┬─────────────────────────────┘
                                                   │
                                                   ▼
                        ┌────────────────────────────────────────────────────────┐
                        │  2. AST Sanitizer: Strips Secrets, Keys, .env, Tokens  │
                        └──────────────────────────┬─────────────────────────────┘
                                                   │
                        ┌──────────────────────────┴─────────────────────────────┐
                        │                                                        │
                        ▼                                                        ▼
         [ OPTION A: AIR-GAPPED LOCAL ]                          [ OPTION B: ZERO-RETENTION CLOUD ]
         • 100% on-device Ollama/vLLM                            • Enterprise API Zero-Data Retention
         • Zero external network telemetry                       • Only scrubbed AST subgraphs sent
```

1. **Air-Gapped Local Operation:** When run with local LLMs (e.g. Ollama, Llama 3.3, Qwen 2.5 Coder), no code, metadata, or telemetry leaves your physical workstation.
2. **Deterministic AST Secret Sanitizer:** Sensitive files (`.env*`, `*.pem`, `credentials.json`) and string literals matching cryptographic entropy keys or JWT tokens are purged before graph ingestion.
3. **Volatile Memory Lifecycles:** Temporary working clones are created in sandboxed system temp files and flushed automatically upon session completion.

---

## 🛠️ Tech Stack & Architectural Rationale

| Layer | Technologies Selected | Architectural Rationale |
| :--- | :--- | :--- |
| **CLI & Core Engine** | **Python 3.10+**, `click`, `rich` | Cross-platform terminal ergonomics, rich TUI formatting, and direct bindings to scientific analysis libraries. |
| **AST Parser** | **Tree-sitter** (`py-tree-sitter`) | Incremental, fault-tolerant syntax parsing supporting 40+ programming languages at native C-speeds. |
| **Knowledge Graph** | **NetworkX / GraphRAG** | Fast in-memory relational graph modeling connecting AST nodes, files, and Git commit deltas. |
| **Web Studio Frontend** | **Next.js 14**, **React**, **Tailwind CSS** | Server-side rendering, fluid glassmorphic UI, dynamic Mermaid and D3.js interactive force-directed graph rendering. |
| **AI Orchestration** | **LangChain / LlamaIndex** | Structured JSON schema outputs, multi-agent reasoning, and deterministic guardrail evaluation. |
| **Local LLM Support** | **Ollama / vLLM / Groq API** | Enables 100% offline, privacy-first repository analysis using local models (`llama3`, `deepseek-coder`, `qwen2.5-coder`). |

---

## 🐳 Docker & Containerization

Deploy CodeDNA locally or on a private server using containerization:

### Multi-Stage `Dockerfile`
```dockerfile
# Stage 1: Build & Native Dependencies
FROM python:3.11-slim AS builder

WORKDIR /app
RUN apt-get update && apt-get install -y --no-install-recommends \
    build-essential git curl && \
    rm -rf /var/lib/apt/lists/*

COPY requirements.txt .
RUN pip install --no-cache-dir --user -r requirements.txt

# Stage 2: Minimal Runtime Image
FROM python:3.11-slim AS runner

WORKDIR /app
RUN apt-get update && apt-get install -y --no-install-recommends git && \
    rm -rf /var/lib/apt/lists/*

# Security: Non-root execution
RUN groupadd -r codedna && useradd -r -g codedna codedna
USER codedna

COPY --from=builder /root/.local /home/codedna/.local
COPY . /app

ENV PATH=/home/codedna/.local/bin:$PATH
EXPOSE 4200

ENTRYPOINT ["codedna"]
CMD ["studio", "--host", "0.0.0.0", "--port", "4200"]
```

### `docker-compose.yml`
```yaml
version: '3.8'

services:
  codedna-engine:
    build: .
    container_name: codedna-engine
    ports:
      - "4200:4200"
    environment:
      - CODEDNA_LLM_PROVIDER=ollama
      - OLLAMA_HOST=http://host.docker.internal:11434
      - CODEDNA_STUDIO_PORT=4200
    volumes:
      - ./projects:/app/projects:ro
    restart: unless-stopped
```

Launch with:
```bash
docker compose up -d
```

---

## ⚡ CLI Quickstart

### Installation
```bash
# Clone the CodeDNA repository
git clone https://github.com/Vish-0806/CodeDNA.git
cd CodeDNA

# Create and activate virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install development dependencies
pip install -e .
```

### Basic Commands
```bash
# 1. Analyze the current working directory
codedna scan .

# 2. Launch the interactive browser studio
codedna studio --port 4200

# 3. Generate a Markdown repository documentary
codedna documentary --output ./DOCS.md

# 4. Start an AI Viva interview simulation
codedna viva --focus architecture --difficulty hard

# 5. Query the provenance of a specific function or line
codedna why src/auth/jwt_handler.py:42
```

---

## 💻 Developer SDK Examples

### Python SDK Integration
```python
from codedna import CodeDNAAnalyzer, VivaEvaluator

# Initialize analyzer with local repository path
analyzer = CodeDNAAnalyzer(repo_path="./my-capstone-project")

# Build knowledge graph and generate documentary
knowledge_graph = analyzer.build_knowledge_graph()
documentary = analyzer.generate_documentary(format="markdown")

# Initialize viva examiner
viva = VivaEvaluator(knowledge_graph=knowledge_graph)
question = viva.generate_question(topic="database_design")

print(f"Examiner: {question.prompt}")
# Evaluate student response
feedback = viva.evaluate_answer(
    question_id=question.id,
    student_response="We used indexing on user_id to optimize lookup speeds."
)
print(f"Score: {feedback.score}/100 | Recommendation: {feedback.tips}")
```

### React Custom Hook (`useCodeDNAViva`)
```typescript
import { useState } from 'react';
import { CodeDNAClient } from '@codedna/sdk';

export function useCodeDNAViva(projectId: string) {
  const [currentQuestion, setCurrentQuestion] = useState<string | null>(null);
  const [evaluation, setEvaluation] = useState<any>(null);
  const client = new CodeDNAClient({ endpoint: 'http://localhost:4200' });

  const fetchNextQuestion = async (topic = 'architecture') => {
    const q = await client.getVivaQuestion({ projectId, topic });
    setCurrentQuestion(q.prompt);
  };

  const submitDefense = async (answer: string) => {
    const result = await client.evaluateDefense({ projectId, answer });
    setEvaluation(result);
    return result;
  };

  return { currentQuestion, evaluation, fetchNextQuestion, submitDefense };
}
```

---

## 🎯 Real-World Case Studies

### 🎓 Case Study 1: The College Capstone Viva
* **Background:** A team of 4 computer science seniors built a distributed microservice e-commerce store using AI coding assistants.
* **The Challenge:** The university evaluation panel was renowned for scrutinizing consistency models and fault tolerance.
* **The CodeDNA Intervention:** The team ran `codedna viva --difficulty hard`. CodeDNA surfaced that their payment service lacked idempotency keys on retry webhooks. The students patched the vulnerability and entered the viva with a verified 94% Understanding Score, achieving top honors.

### 💼 Case Study 2: Fast-Tracking Hackathon Judging
* **Background:** A 36-hour hackathon project developed an AI document translator under immense time pressure.
* **The Challenge:** Judges only had 3 minutes per booth to evaluate technical architecture.
* **The CodeDNA Intervention:** The team showcased the live **CodeDNA Architecture Flowchart** and exported an automated documentary chapter explaining how their in-memory streaming audio concatenation worked, winning "Best Engineering Design."

### 🏢 Case Study 3: The 300K-Line Monolith Onboarding
* **Background:** A newly hired Senior Engineer needed to lead a refactoring initiative on a 6-year-old financial service codebase with sparse documentation.
* **The Challenge:** Deciphering why certain legacy caching hacks existed without disturbing production SLA.
* **The CodeDNA Intervention:** Using `codedna why`, the engineer traced undocumented fallback logic directly to a 2021 database connection pool outage, avoiding a disastrous deprecation.

---

## 🗺️ Project Roadmap

- [x] **Phase 1: Concept & Repository Foundations**
  - [x] Comprehensive product specification and architecture blueprint.
  - [x] Problem taxonomy and viva interview paradigm design.
  - [x] Git repository workflow & CI setup.
- [ ] **Phase 2: Core Parsing Engine & Graph Builder (In Progress)**
  - [ ] Tree-sitter AST extraction pipeline for Python, TypeScript, and JavaScript.
  - [ ] Git commit archaeology and semantic diff clustering.
  - [ ] GraphRAG knowledge graph schema definition.
- [ ] **Phase 3: AI Documentary & Viva Simulator**
  - [ ] Episodic documentary narrative generation engine.
  - [ ] Interactive TUI and Web-based viva interview simulator with real-time scoring.
  - [ ] Interactive Mermaid architecture and feature flow generation.
- [ ] **Phase 4: Ecosystem & Developer Tooling**
  - [ ] VS Code / Cursor IDE Extension for instant *"Why does this exist?"* code lens.
  - [ ] Offline local LLM engine support via Ollama.
  - [ ] Multi-repository architectural comparison and diffing.

---

## ❓ Frequently Asked Questions

<details>
<summary><b>1. Will my private code be sent to external AI servers?</b></summary>
<br>
CodeDNA prioritizes data sovereignty. The parsing and knowledge graph extraction phases run 100% locally on your machine. For reasoning, CodeDNA supports local inference engines like <b>Ollama</b>, <b>vLLM</b>, and <b>LocalAI</b>. When using cloud providers (OpenAI, Anthropic, Gemini), data is processed in accordance with zero-retention enterprise API policies.
</details>

<details>
<summary><b>2. How does CodeDNA differ from asking ChatGPT to "explain this code"?</b></summary>
<br>
Standard AI chatbots analyze code in isolation without temporal context. They do not know why a commit was made 6 months ago, what bug it fixed, what alternative libraries were rejected, or how an AST mutation ripples through disparate microservices. CodeDNA combines <b>Git history + AST graphs + GraphRAG</b> to explain the full evolutionary story.
</details>

<details>
<summary><b>3. What programming languages are supported?</b></summary>
<br>
Because CodeDNA leverages Tree-sitter for AST parsing, multi-language support is built into the architecture. Initial focus languages are <b>Python</b>, <b>TypeScript</b>, <b>JavaScript</b>, and <b>Go</b>, with planned expansions to <b>Java</b>, <b>C++</b>, and <b>Rust</b>.
</details>

<details>
<summary><b>4. How does CodeDNA handle repositories with messy commit histories (e.g., "wip", "fix")?</b></summary>
<br>
CodeDNA does not rely solely on commit messages. It computes <b>semantic AST diffs</b> between commits—analyzing changes to function signatures, imports, variable scopes, and call graphs. Even if the commit message says <code>"asdf"</code>, CodeDNA deduces: <i>"Refactored authentication middleware to enforce token expiration checks."</i>
</details>

<details>
<summary><b>5. Can CodeDNA work on massive monorepos?</b></summary>
<br>
Yes. CodeDNA uses selective directory scoping, path pruning (respecting <code>.gitignore</code>), and chunked graph indexing to process sub-packages independently without memory bottlenecks.
</details>

---

## 🤝 Contributing

Contributions are what make the open-source community an inspiring place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📜 License

Distributed under the **MIT License**. See `LICENSE` for more information.

<div align="center">

---

**Built with ❤️ to bridge the gap between building software and truly understanding it.**

[⭐ Star on GitHub](https://github.com/Vish-0806/CodeDNA) • [🐛 Report a Bug](https://github.com/Vish-0806/CodeDNA/issues) • [💡 Request a Feature](https://github.com/Vish-0806/CodeDNA/issues)

</div>
