Systems engineer focused on **databases, distributed systems, and high-performance backend infrastructure**.

MS in Computer Science at **New York University** · previously Senior Backend Engineer building event-driven platforms for 13M+ users. I like building systems from the primitives up (event loops, hash tables, wire protocols) and composing them into real servers.

<table>
  <tr>
    <td width="25%" valign="top"><h3>&lt;150 ms</h3>p99 latency for an idempotent wallet service, zero double-charges</td>
    <td width="25%" valign="top"><h3>2.66×</h3>over serial PostgreSQL, GPU <code>GROUP BY</code> on 30M TPC-H rows</td>
    <td width="25%" valign="top"><h3>4,000</h3>concurrent chess games on one droplet, zero consistency failures</td>
    <td width="25%" valign="top"><h3>2</h3>Rust crates published on crates.io</td>
  </tr>
</table>

## Things I've built

#### `crates.io` Published Rust crates ([arrxy](https://crates.io/users/arrxy))

- **[chaintable](https://github.com/arrxy/chaintable)** — SwissTable-style hash map with exact **O(1) uniform-random key sampling** (the primitive Redis eviction needs). SIMD group probing (NEON/SSE2), incremental rehashing, LRU/LFU/random eviction.
- **[pollio](https://github.com/arrxy/poll-io)** — zero-dependency event poller unifying Linux **epoll** and macOS **kqueue** behind one safe `Poller` trait, written directly against `libc` via unsafe FFI.

#### `systems` Built from those primitives

- **[fast_kv](https://github.com/arrxy/FastKV)** — Redis-compatible in-memory KV store speaking the RESP wire protocol, built on my own two crates above: pollio event loop + chaintable sampled-eviction store. Hand-rolled RESP codec with pipelining, TTL semantics, Redis upstream tests ported to Rust.
- **[Parallel Chess](https://github.com/arrxy/chess-engine)** — horizontally scalable real-time multiplayer chess server (Rust/Axum, sharded Valkey, MongoDB). Optimistic CAS instead of distributed locks; zero consistency failures across millions of load-tested moves. [Case study](https://github.com/arrxy/chess-engine/blob/master/findings/finding.md) · live at [chess.socketlab.tech](https://chess.socketlab.tech)

#### `databases` Search and query engines

- **[Indexify](https://github.com/arrxy/indexify)** — terminal document search over local PDF, Markdown and DOCX, on a from-scratch disk-backed search engine in Rust: Simple9-compressed postings, exact BM25 AND/OR retrieval, Metal GPU radix sort. Indexes 8.84M MS MARCO passages (3.06 GB) in 55 s on an Apple M4.
- **[pg_flux](https://github.com/arrxy/pg_flux)** — PostgreSQL extension that offloads integer `GROUP BY` aggregation to NVIDIA GPUs through planner hooks and `CustomScan`, without touching core. 2.66× over serial PostgreSQL on 30M TPC-H rows (C++17, CUDA, CUB).

#### `ml` AI systems

- **[Persona AI](https://github.com/arrxy/persona-agent)** — full-stack RAG platform turning YouTube creators' public captions into chattable personas (Qdrant, layered context budgeting, durable user memory). Live at [persona-agent.aritro.me](https://persona-agent.aritro.me)
- **[PhotoPrism MLOps](https://github.com/arrxy/photoprism-mlops)** — semantic photo search with continuous learning: CLIP retrieval + Qwen2-VL-2B LoRA reranker auto-retraining from implicit clicks, on Kubernetes (Chameleon Cloud). Published the **[Flickr30K-CFQ](https://huggingface.co/datasets/ar10067/flickr30k-images-CFQ)** retrieval benchmark on HuggingFace. [Deep dive](https://www.aritro.me/projects/photoprism-mlops)

## Open source

- **[ParadeDB](https://github.com/paradedb/paradedb)** (Postgres BM25 extension, Rust) — Custom Scan heap-filter fallback for unsupported Boolean predicates; `citext` indexing support
- **[libprocessing](https://github.com/processing/libprocessing)** (Rust/Bevy/WebGPU) — fixed logical-vs-physical pixel handling for HiDPI/Retina across GLFW + Bevy; building CPU/GPU benchmarking infra
- **Corelink Audio Transport** (C++/JUCE) — multithreaded audio networking with lock-free queues; ANIRA-based adaptive packet-loss concealment

## In production

- Backend systems serving **13M+ users** (founding engineer, Web3 questing platform)
- Kafka event pipelines at **10K+ events/min** with 100-level referral chains
- Idempotent payments (p99 <150ms, zero double-charges), media pipelines at 50K+ jobs/day
- Real-time AI voice interviews at 100 concurrent sessions (OpenAI Realtime API + LiveKit)
- 3,000+ hours of tracked coding via WakaTime

## Writing

- [I Couldn't Overwhelm My Chess Server. I Could Only Overwhelm My Load Tester.](https://www.aritro.me/blogs/distributed-chess-server) · `distributed systems`
- [The log factor isn't free: a Dijkstra rabbit hole](https://www.aritro.me/blogs/dijkstra-radix-heap) · `performance`
- [The Mathematical Backbone of AI Agents: Finite Markov Decision Processes](https://www.aritro.me/blogs/markov-decision-process) · `AI agents`

More at [aritro.me/blogs](https://www.aritro.me/blogs).

## Stack

| | |
| :-- | :-- |
| **Languages** | `Rust` `C++` `TypeScript` `Python` `Java` |
| **Data** | `PostgreSQL` `Redis` `MongoDB` `MySQL` `DynamoDB` `SQLite` |
| **Messaging** | `Kafka` `RabbitMQ` |
| **Cloud & infra** | `AWS` `Kubernetes` `Docker` `DigitalOcean` `OpenStack` `Nginx` |
| **ML** | `CUDA` `PyTorch` `MLflow` `NumPy` `OpenCV` |
| **Web** | `Node.js` `Express` `NestJS` `Next.js` `JWT` |

## Say hello

[aritro.me](https://www.aritro.me) · [LinkedIn](https://linkedin.com/in/aritro-roy19) · [X](https://x.com/Aritro_ry) · [YouTube](https://youtube.com/@codetherapy99) · [Email](mailto:aritroroy1999@gmail.com)

[![WakaTime](https://wakatime.com/badge/user/a9c8507b-e2a1-46bc-845b-6148e53e6f1a.svg)](https://wakatime.com/@arrxy)
