## Chayathorn Puchana

Computer Science student at KMITL, also studying accounting at Ramkhamhaeng University, Bangkok.
I have run my own online shop for five years and build the software behind it. I like back-end code
that keeps working when things around it fail, and tests that prove it does.

### Projects

| Project | What it is | The part I'm proudest of |
|---|---|---|
| [llm-toolkit](https://github.com/LPKKHEATHER3/llm-toolkit) | Python building blocks for LLM tools: multi-provider client, tool-calling agent, BM25 RAG with quote verification, eval harness, MCP server | CI on Linux caught a connection-reset bug that never showed on Windows; traced it to the listen backlog (21/25 failing runs → 0/25) |
| [sql-engine](https://github.com/LPKKHEATHER3/sql-engine) | A dependency-free SQL `SELECT` interpreter in JavaScript, with a [browser playground](https://lpkkheather3.github.io/sql-engine/demo/) | Checked against real SQLite with a seeded fuzzer: 52,000 random queries, 0 mismatches |
| [inventory-manager](https://github.com/LPKKHEATHER3/inventory-manager) | Small-shop inventory system on Python's standard library | Every change is a transaction; multi-step undo that refuses to undo someone else's change |
| [emuvision](https://github.com/LPKKHEATHER3/emuvision) | Screen-driven automation toolkit for Android emulators | One guarded layer sends all input and refuses to tap anywhere it was told not to |

### How I work

I build with Claude Code as a pair programmer. I write the spec, review every change, and make the
tests and CI decide whether it is done.

**Languages and tools:** Python · JavaScript · Java · SQL · pytest · Hypothesis · GitHub Actions · MCP · OpenCV
