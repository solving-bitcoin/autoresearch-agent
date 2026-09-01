# Solving Bitcoin

**Autonomous research for Bitcoin protocols.**

Solving Bitcoin is an experimental research effort for discovering, testing, and improving Bitcoin constructions.

The goal is to build research systems that can move from **literature → hypothesis → implementation → experiment → verification**, grounded in primary sources and executable against Bitcoin itself.

## Research Loop

```text
Research → Construct → Execute → Verify → Improve
```

Research agents combine Bitcoin protocol literature, cryptography research, existing constructions, and [Bitcoin Core](https://github.com/bitcoin/bitcoin) source code to propose and investigate ideas.

Those ideas are then implemented and tested in reproducible local environments rather than evaluated through reasoning alone.

## Research Infrastructure

### Knowledge Base

A versioned, citation-grounded research library spanning:

* **Bitcoin Script primitives**

  * [Solving Bitcoin / bitcoin-scripts](https://github.com/solving-bitcoin/bitcoin-scripts)
  * [Bitcoin Wiki — Script](https://en.bitcoin.it/wiki/Script)
  * [Bitcoin Core](https://github.com/bitcoin/bitcoin) for implementation-level reference

* **Bitcoin protocol research**

  * [Bitcoin Development Mailing List](https://groups.google.com/g/bitcoindev)
  * [Delving Bitcoin](https://delvingbitcoin.org/)
  * [BitcoinTalk](https://bitcointalk.org/)
  * Papers, protocol proposals, implementations, and historical discussions
  * [Bitcoin Knowledge Base](https://bitcoinknowledge.dev/) for agent-queryable Bitcoin and Lightning development knowledge

* **Cryptography research**

  * [IACR Cryptology ePrint Archive](https://eprint.iacr.org/)
  * [IACR ePrint MCP server](https://github.com/heewon-chung/eprint-mcp-server)
  * [arXiv](https://arxiv.org/)
  * [alphaXiv MCP](https://www.alphaxiv.org/docs/mcp)
  * Cryptography textbooks, consensus papers, and specialized cryptography research agents

* **Protocol implementation**

  * [Bitcoin Core](https://github.com/bitcoin/bitcoin) as the reference implementation
  * [Bitcoin Core developer documentation](https://doxygen.bitcoincore.org/)
  * [`rust-bitcoin`](https://github.com/rust-bitcoin/rust-bitcoin) for Bitcoin experimentation in Rust

Research agents provide literature discovery, source retrieval, citation tracking, synthesis, code inspection, and cross-referencing across these collections.

### Experimental Environment

Research should produce executable artifacts.

The lab provides tools for:

* Bitcoin Script execution and tracing
* [`rust-bitcoin`](https://github.com/rust-bitcoin/rust-bitcoin) experimentation
* [Bitcoin Core](https://github.com/bitcoin/bitcoin) and `libbitcoinkernel`
* Local Bitcoin Core regtest nodes
* Automated testing and benchmarking
* Reproducible protocol experiments

Research can be orchestrated through model-agnostic agents such as [OpenCode](https://opencode.ai/), allowing different hosted or local models to work against the same research and experimentation infrastructure.

The environment is designed to be **local, inspectable, citation-grounded, reproducible, and model-agnostic**.

## Research Roadmap

### 1. Optimize existing primitives

Search the space of known constructions for implementations that are smaller, cheaper, faster, or otherwise better.

These problems have objective evaluation functions and parallelize well, making them useful early targets for autonomous research.

Related optimization competitions include:

* [zk.golf](https://zk.golf/)
* [Yukon](https://www.yukon.org/)

### 2. Invent new Bitcoin Script primitives

Discover reusable constructions that can be expressed using Bitcoin's existing scripting and transaction capabilities.

The output is not just an idea, but ideally an implementation, test vectors, benchmarks, and an explanation of why the construction works.

### 3. Invent new Bitcoin protocols

Compose existing and newly discovered primitives into novel protocols with useful security, privacy, scalability, or functionality properties.

Research agents should be able to move between literature, Bitcoin Core behavior, implementation, adversarial analysis, and experiments when evaluating a protocol.

### 4. Explore new cryptographic primitives

Longer term, apply the same research loop to cryptographic constructions themselves.

```text
Search → Construct → Attack → Test → Verify → Improve
```

Potential evaluation tools include automated adversarial testing, fuzzing, formal verification, benchmarks, and proofs of soundness.

## Principles

**Ground research in sources.**
Claims should be traceable to papers, technical discussions, code, or experimental evidence.

**Run the idea.**
A construction should be executable wherever possible.

**Use Bitcoin Core as ground truth.**
Protocol reasoning should ultimately be checked against the reference implementation.

**Make experiments reproducible.**
Sources, software revisions, test environments, and results should be inspectable and repeatable.

**Separate evidence from speculation.**
Research agents should make clear whether a conclusion comes from primary sources, implementation behavior, experimental evidence, or a new hypothesis.

**Optimize before inventing.**
Start with problems that have clear evaluation functions, then progressively move toward more open-ended discovery.

---

**Research → Construct → Execute → Verify → Improve**
