### Hi, I'm Aritro

Systems Engineer focused on **databases, distributed systems, and high-performance backend infrastructure**.

MS in Computer Science at **New York University** · previously Senior Backend Engineer building event-driven platforms for 13M+ users. I like building systems from the primitives up — event loops, hash tables, wire protocols — and composing them into real servers.

---

#### Things I've Built

**Published Rust crates** ([crates.io](https://crates.io/users/arrxy))

- **[chaintable](https://github.com/arrxy/chaintable)** — SwissTable-style hash map with exact **O(1) uniform-random key sampling** (the primitive Redis eviction needs). SIMD group probing (NEON/SSE2), incremental rehashing, LRU/LFU/random eviction.
- **[pollio](https://github.com/arrxy/poll-io)** — zero-dependency event poller unifying Linux **epoll** and macOS **kqueue** behind one safe `Poller` trait, written directly against `libc` via unsafe FFI.

**Systems from those primitives**

- **[fast_kv](https://github.com/arrxy/FastKV)** — Redis-compatible in-memory KV store speaking the RESP wire protocol, built on my own two crates above: pollio event loop + chaintable sampled-eviction store. Hand-rolled RESP codec with pipelining, TTL semantics, Redis upstream tests ported to Rust.
- **[Parallel Chess](https://github.com/arrxy/chess-engine)** — horizontally scalable real-time multiplayer chess server (Rust/Axum, sharded Valkey, MongoDB). Optimistic CAS instead of distributed locks; zero consistency failures across millions of load-tested moves. [Case study](https://github.com/arrxy/chess-engine/blob/master/findings/finding.md) · live at chess.socketlab.tech

**AI systems**

- **[Persona AI](https://github.com/arrxy/persona-agent)** — full-stack RAG platform turning YouTube creators' public captions into chattable personas (Qdrant, layered context budgeting, durable user memory). Live at [persona-agent.aritro.me](https://persona-agent.aritro.me)
- **[PhotoPrism MLOps](https://github.com/arrxy/photoprism-mlops)** — semantic photo search with continuous learning: CLIP retrieval + Qwen2-VL-2B LoRA reranker auto-retraining from implicit clicks, on Kubernetes (Chameleon Cloud). Published the **[Flickr30K-CFQ](https://huggingface.co/datasets/ar10067/flickr30k-images-CFQ)** retrieval benchmark on HuggingFace.

---

#### Open Source Contributions

- **ParadeDB** (Postgres BM25 extension, Rust) — Custom Scan heap-filter fallback for unsupported Boolean predicates; `citext` indexing support
- **libprocessing** (Rust/Bevy/WebGPU) — fixed logical-vs-physical pixel handling for HiDPI/Retina across GLFW + Bevy; building CPU/GPU benchmarking infra
- **Corelink Audio Transport** (C++/JUCE) — multithreaded audio networking with lock-free queues; ANIRA-based adaptive packet-loss concealment

---

#### Production Experience

- Backend systems serving **13M+ users** (founding engineer, Web3 questing platform)
- Kafka event pipelines at **10K+ events/min** with 100-level referral chains
- Idempotent payments (p99 <150ms, zero double-charges), media pipelines at 50K+ jobs/day
- Real-time AI voice interviews at 100 concurrent sessions (OpenAI Realtime API + LiveKit)
- 3,000+ hours of tracked coding via WakaTime

---

#### Writing

Technical deep-dives at [aritro.me](https://www.aritro.me) — distributed systems, database internals, performance engineering.

---

### Socials:
[![LinkedIn](https://img.shields.io/badge/LinkedIn-%230077B5.svg?logo=linkedin&logoColor=white)](https://linkedin.com/in/aritro-roy19) [![YouTube](https://img.shields.io/badge/YouTube-%23FF0000.svg?logo=YouTube&logoColor=white)](https://youtube.com/@codetherapy99) [![email](https://img.shields.io/badge/Email-D14836?logo=gmail&logoColor=white)](mailto:aritroroy1999@gmail.com)
[![WakaTime](https://wakatime.com/badge/user/a9c8507b-e2a1-46bc-845b-6148e53e6f1a.svg)](https://wakatime.com/@arrxy)
[![Portfolio](https://img.shields.io/badge/Portfolio-000000?logo=vercel&logoColor=white)](https://www.aritro.me)

### Tech Stack:
![Rust](https://img.shields.io/badge/rust-%23000000.svg?style=for-the-badge&logo=rust&logoColor=white) ![C++](https://img.shields.io/badge/c++-%2300599C.svg?style=for-the-badge&logo=c%2B%2B&logoColor=white) ![TypeScript](https://img.shields.io/badge/typescript-%23007ACC.svg?style=for-the-badge&logo=typescript&logoColor=white) ![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54) ![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white) ![Postgres](https://img.shields.io/badge/postgres-%23316192.svg?style=for-the-badge&logo=postgresql&logoColor=white) ![Redis](https://img.shields.io/badge/redis-%23DD0031.svg?style=for-the-badge&logo=redis&logoColor=white) ![MongoDB](https://img.shields.io/badge/MongoDB-%234ea94b.svg?style=for-the-badge&logo=mongodb&logoColor=white) ![MySQL](https://img.shields.io/badge/mysql-4479A1.svg?style=for-the-badge&logo=mysql&logoColor=white) ![AmazonDynamoDB](https://img.shields.io/badge/Amazon%20DynamoDB-4053D6?style=for-the-badge&logo=Amazon%20DynamoDB&logoColor=white) ![SQLite](https://img.shields.io/badge/sqlite-%2307405e.svg?style=for-the-badge&logo=sqlite&logoColor=white) ![Apache Kafka](https://img.shields.io/badge/Apache%20Kafka-000?style=for-the-badge&logo=apachekafka) ![RabbitMQ](https://img.shields.io/badge/rabbitmq-FF6600?style=for-the-badge&logo=rabbitmq&logoColor=white) ![AWS](https://img.shields.io/badge/AWS-%23FF9900.svg?style=for-the-badge&logo=amazon-aws&logoColor=white) ![Kubernetes](https://img.shields.io/badge/kubernetes-%23326ce5.svg?style=for-the-badge&logo=kubernetes&logoColor=white) ![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white) ![DigitalOcean](https://img.shields.io/badge/DigitalOcean-%230167ff.svg?style=for-the-badge&logo=digitalOcean&logoColor=white) ![OpenStack](https://img.shields.io/badge/Openstack-%23f01742.svg?style=for-the-badge&logo=openstack&logoColor=white) ![nVIDIA](https://img.shields.io/badge/cuda-000000.svg?style=for-the-badge&logo=nVIDIA&logoColor=green) ![PyTorch](https://img.shields.io/badge/PyTorch-%23EE4C2C.svg?style=for-the-badge&logo=PyTorch&logoColor=white) ![mlflow](https://img.shields.io/badge/mlflow-%23d9ead3.svg?style=for-the-badge&logo=numpy&logoColor=blue) ![NodeJS](https://img.shields.io/badge/node.js-6DA55F?style=for-the-badge&logo=node.js&logoColor=white) ![Express.js](https://img.shields.io/badge/express.js-%23404d59.svg?style=for-the-badge&logo=express&logoColor=%2361DAFB) ![NestJS](https://img.shields.io/badge/nestjs-%23E0234E.svg?style=for-the-badge&logo=nestjs&logoColor=white) ![Next JS](https://img.shields.io/badge/Next-black?style=for-the-badge&logo=next.js&logoColor=white) ![Nginx](https://img.shields.io/badge/nginx-%23009639.svg?style=for-the-badge&logo=nginx&logoColor=white) ![JWT](https://img.shields.io/badge/JWT-black?style=for-the-badge&logo=JSON%20web%20tokens) ![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white) ![OpenCV](https://img.shields.io/badge/opencv-%23white.svg?style=for-the-badge&logo=opencv&logoColor=white)
