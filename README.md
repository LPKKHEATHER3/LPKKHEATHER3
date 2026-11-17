<div align="center">

# Chayathorn Puchana

**I build back-end code that keeps working when the things around it fail, and tests that prove it.**

Computer Science at KMITL · Accounting at Ramkhamhaeng University · Bangkok, Thailand

Looking for a **Summer 2027 internship** in back-end or LLM tooling

</div>

---

### About

I have run my own online shop since 2021, alongside school, and I write the software it runs on:
the storefront, the stock tooling, the automation behind it. Real customers taught me that the
expensive bugs are the quiet ones, so most of what I build is about failing loudly and safely.

Three habits you will find in every repo below:

- **Refuse rather than guess.** OCR returns "unsure" instead of a believable wrong number; a citation
  that is not a verbatim quote gets dropped; an input layer refuses to tap where it was told not to.
- **Let tests decide when it is done.** Each repo has an offline test suite that runs in CI on every push.
- **Check against something real.** The SQL engine is compared with SQLite; the LLM eval keeps
  provider outages apart from model mistakes.

---

### Featured projects

#### [llm-toolkit](https://github.com/LPKKHEATHER3/llm-toolkit) · Python
Building blocks for LLM features: a client over OpenRouter, Google AI Studio and the Anthropic API
with retry, failover and a deadline per request; a tool-calling agent; BM25 RAG whose answers must
quote their sources verbatim; an eval harness; and an MCP server that lets an agent manage stock in
inventory-manager.

> **Proof:** 188 offline tests. CI on Ubuntu caught a connection-reset bug that never appeared on
> Windows. I reproduced it on Linux, traced it to the listen backlog, and fixed it: 21 of 25 runs
> failing before, 0 of 25 after.

`httpx` · `pydantic` · `MCP` · `pytest` · `Hypothesis` · `GitHub Actions`

#### [sql-engine](https://github.com/LPKKHEATHER3/sql-engine) · JavaScript · [live playground](https://lpkkheather3.github.io/sql-engine/demo/)
A dependency-free SQL `SELECT` interpreter: joins of every kind, grouping, correlated subqueries
and proper three-valued NULL logic, plus a strict mode that flags queries SQLite silently accepts.

> **Proof:** every result is checked against real SQLite. A seeded fuzzer ran 52,000 random queries
> with 0 mismatches, after the comparison uncovered and I fixed 5 correctness bugs.

`Node.js` · `sql.js` · `Python` (normalization checker)

#### [inventory-manager](https://github.com/LPKKHEATHER3/inventory-manager) · Python standard library
A small-shop inventory system: SKUs, stock movements, a trash bin, duplicate detection, CSV
import/export and printable label cards, served by a REST API with no framework.

> **Proof:** every change is a transaction; undo refuses to reverse someone else's change; CSV import
> is all-or-nothing; static files are protected against path traversal and symlink escapes. 30 tests.

`http.server` · `vanilla JS` · `unittest`

#### [emuvision](https://github.com/LPKKHEATHER3/emuvision) · Python
The open-sourced engine of my shop's automation system, which turned a 4–5 day manual job into an
overnight run: fast screen capture through `ctypes`, OpenCV matching, guarded OCR, and one layer that
sends all input.

> **Proof:** 20 tests that run without a device, because input and screen capture are injected.

`OpenCV` · `NumPy` · `ctypes` · `adb`

---

<sub>I build with Claude Code as a pair programmer: I write the spec, review every change, and let the tests and CI decide.</sub>
