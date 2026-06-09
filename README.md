# Adam Sacks — Applied AI Portfolio

*Self-built, working AI systems — shipped solo, on nights and weekends.*

📍 Evergreen, CO · ✉️ asacks3@gmail.com

> Applied-AI engineer with 16 years in finance who builds and ships. By day I introduced agentic AI to a $1B+ medical-device company and drove it into production. By night I build the systems below — on my own hardware, with AI-native tooling — to stay on the edge of what's possible.

---

## 🧠 Cortex — Local AI Sensory System
**Problem:** Real-time, private home awareness and offline AI that keeps working when the internet (or the grid) goes down — without streaming camera feeds to anyone's cloud.

**What I built:** A single FastAPI service (15+ endpoints) that fuses vision, speech, retrieval, and event analytics, fronted by an agent that routes each query to the right capability and degrades gracefully offline.

**Stack:** Python / FastAPI · YOLOv8 object detection on CUDA · Whisper speech-to-text · ChromaDB vector knowledge · SQLite event log with LLM-powered anomaly detection · multi-camera NVR integration · cloud LLM for heavy reasoning with a local-LLM fallback when offline.

**What it shows:** I ship complex, multi-model AI end to end — vision + audio + retrieval + an orchestration agent — wired into real hardware, with graceful offline degradation and false-alarm suppression.

*Live demo and architecture diagram available on request.*

---

## 🔎 NHTSA Hybrid Search — Semantic + Relational over 2.4M rows
**Problem:** Public vehicle-safety data is huge, messy, and nearly impossible to search by *meaning*.

**What I built:** Loaded **240,846 recalls + 2,210,945 complaints** from raw NHTSA flat files into SQL Server 2025, generated 768-dimension embeddings *in the database*, and built hybrid search that blends semantic vector search with hard relational filters (make / model / year / crash / fire).

**Stack:** SQL Server 2025 (native VECTOR + DiskANN) · in-database embeddings via a local Ollama model · T-SQL · a reusable PowerShell embedding loader I wrote.

**What it shows:** Extracting signal from imperfect, large-scale real-world inputs — then turning it into a working, queryable AI product.

→ *Code repo: publishing shortly*

---

## 📚 Local RAG — Offline Knowledge Engine
**Problem:** Trustworthy answers from a private knowledge base with zero internet dependency.

**What I built:** A fully offline RAG application (web + CLI) with query rewriting and an answer style tuned for direct, actionable responses.

**Stack:** Ollama (Qwen family) · nomic-embed embeddings · ChromaDB · Streamlit + CLI · incremental indexing with file-watch.

**What it shows:** Retrieval-quality engineering — query rewriting, collection design to stay stable at scale — the same craft behind the 78,000-document RAG suite I shipped at work.

→ *Code repo: publishing shortly*

---

## 🤖 Pi Claw — Self-Hosted AI Assistant on a Raspberry Pi
**Problem:** A private AI assistant I can message from anywhere, running on cheap hardware.

**What I built:** A self-hosted LLM assistant on a Raspberry Pi 5 (8GB) that I talk to over Signal — end-to-end encrypted — running a local model behind a sub-second-boot agent gateway.

**Stack:** Raspberry Pi 5 · PicoClaw (lightweight Go agent gateway) · Ollama + Qwen 2.5 · signal-cli.

**What it shows:** Shipping on constrained edge hardware, security-first.

---

## 🏕️ RecreationGov Layered Search
Multi-vector semantic search over 5,531 campgrounds, each carrying **three independent embeddings** (description / directions / activities), ranked by a weighted blend — change the "what do you want to do" facet and results re-rank while the "vibe" query stays fixed.

→ *Code repo: publishing shortly*

---

*More repos being published. Demos and architecture diagrams available on request.*
