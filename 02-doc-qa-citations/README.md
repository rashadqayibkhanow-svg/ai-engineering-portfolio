# Doc-QA with Citations  🚧 Stage A

A document-question-answering system that answers **only** from retrieved source spans, and returns a **citation receipt** (`{source: chunk_id, quote: exact_text}`) so every answer is verifiable. It separates *exact source support* from *mere relevance* — the difference between a grounded answer and a hallucination.

Built while working through the Applied-AI-Engineer path of [AI Engineering from Scratch](https://github.com/rohitg00/ai-engineering-from-scratch) (project `doc-qa-with-citations`), then grown into my own version with an evaluation harness and cost tracking.

## Plan (grown in stages)
- **Stage A — RAG core:** load local docs with stable provenance, rank chunks, accept only grounded answers, return citations.
- **Stage B — Evals:** an eval harness that proves a deliberately planted wrong answer gets *caught*. (This is the hire-maker.)
- **Stage C — Reliability + cost:** fallback model, latency/cost-per-answer report, guardrails.

## Skills this builds
Local document loading with provenance · inspectable chunk ranking · grounding gate · framework splitter (`langchain-text-splitters`) without losing offsets · evaluation · cost-per-outcome.

---

## ▶ NEXT ACTION (do this first next window)
1. Read `course/phases/11-llm-engineering/01-prompt-engineering/docs/en.md` (~90 min) — then type and run the lesson code, don't just read it.
2. Read `course/projects/doc-qa-with-citations/README.md` and `API.md`, and look at `stages/` (4 stages) + `solution/` for the shape of the target.
3. Start Stage A: create `src/` here, copy a few sample docs into `data/`, and write the first `query(directory, question, model)` skeleton. Commit it — even broken.

*(venv is at `../.venv`; activate with `source ../.venv/Scripts/activate`. `langchain-text-splitters`, `anthropic`, `openai`, `tiktoken`, `numpy` are already installed.)*
