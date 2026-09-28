# Repolex Knowledge Graph of asimov-modules/asimov-jq-module

RDF knowledge graph data for [asimov-modules/asimov-jq-module](https://github.com/asimov-modules/asimov-jq-module), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [rlex](https://github.com/repolex-ai/rlex) query tool:

```bash
cargo install --git https://github.com/repolex-ai/rlex
```

Verify the install:

```bash
rlex --help
```

**rlex is designed to be used primarily by LLMs in a terminal.** Start up your favorite AI assistant and ask it to use rlex. It handles the SPARQL — you just ask questions in plain English.

To load this repo's data:

```bash
rlex download asimov-modules/asimov-jq-module
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── deea1b3c83a54d5051c62d98ad9168ccabeeb671
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── deea1b3c83a54d5051c62d98ad9168ccabeeb671.nq.gz
│   └── repolex
│       └── deea1b3c83a54d5051c62d98ad9168ccabeeb671
│           └── chunk-001.nq.gz
├── blob
│   ├── 10b359dd05935c73efb064470f9ecda90f6d28aa.nq.gz
│   ├── 152efb1545aff147a1636803589b160a9fd4dae4.nq.gz
│   ├── 2b0c788e2596d934456a7ce78cc4e7f3fe40e217.nq.gz
│   ├── 6b23d61018f43b840f8d2ff3b45a1c02d76df38d.nq.gz
│   ├── 6cb47f93b9af6cac0bba6563e91f82ab7a2404a4.nq.gz
│   ├── 72b76f520755e6d6e6cadf1ae2a647e24f293793.nq.gz
│   ├── 757ffae05f5aba687ee880cb2e8885d47f66c4b2.nq.gz
│   ├── 75e3b65f99b29f48ab230e3eab3de8d0b7a9229f.nq.gz
│   ├── 9faa1b7a7339db85692f91ad4b922554624a3ef7.nq.gz
│   ├── 9fe50de16e59d550235aa6d7d15ee12ddf054414.nq.gz
│   ├── a36fedab8db68b26a76fbbf1de1f549e4a12261b.nq.gz
│   ├── af9908b08f4b33c32a0080af73f53bc0fa0cdce4.nq.gz
│   ├── baa04157e874ddf06c7e756ed563c655b8c123b7.nq.gz
│   ├── c4902839b1bbb1197b10e24c6bd2353248bcef1c.nq.gz
│   ├── cf42f6893594e2f8be2b722de51123d65e4d61c4.nq.gz
│   ├── e1c5410256d55a6915ed89c43abf702d5d6ab309.nq.gz
│   ├── e3e57a8ce4ccbf74759a6df8fa4a3980ff1c9209.nq.gz
│   ├── edfde2f991bd283d2739d5f416b4eb82fe0a5ca0.nq.gz
│   ├── ee4d9362508d63f9e156fe9ee1b11ebc1a3e86d6.nq.gz
│   ├── efb98088164f5786b17e83ed384971fc3c74f93c.nq.gz
│   └── f3b52525a572620ad6aeecd773025cd935158883.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── deea1b3c83a54d5051c62d98ad9168ccabeeb671.nq.gz
├── filetree
│   └── deea1b3c83a54d5051c62d98ad9168ccabeeb671.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 29 files
```

| Directory | What it contains |
|-----------|-----------------|
| `blob/` | Per-file AST graphs, content-addressed by git blob SHA. Each file in the source repo gets its own graph. |
| `aggregate/ast/` | Combined AST graph per parsed commit. Merges all blob graphs for a snapshot of the entire codebase at that point. |
| `aggregate/lsp/` | Language Server Protocol enrichment: resolved symbols, definitions, references, and type information. |
| `aggregate/dataflow/` | Interprocedural data flow edges between functions and modules. |
| `aggregate/repolex/` | Combined graph (AST + LSP + dataflow) per commit. |
| `commit/` | Git commit metadata (author, date, message, parent links). |
| `branch/` | Branch metadata. |
| `tag/` | Tag metadata. |
| `filetree/` | File tree snapshots per commit (which files existed and their blob SHAs). |
| `audit/` | Code architecture and graph audit reports per commit. |

## Source repository

[asimov-modules/asimov-jq-module](https://github.com/asimov-modules/asimov-jq-module)

---
*Parsed on 2026-09-28 by [repolex](https://repolex.ai)*
