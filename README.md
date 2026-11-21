# Repolex Knowledge Graph of princjef/commitlint-azure-pipelines-cli

RDF knowledge graph data for [princjef/commitlint-azure-pipelines-cli](https://github.com/princjef/commitlint-azure-pipelines-cli), parsed by [repolex](https://repolex.ai).

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
rlex download princjef/commitlint-azure-pipelines-cli
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── fc351c5d6efd8dc2be7bb6cdc406412d2e8b76c3
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── fc351c5d6efd8dc2be7bb6cdc406412d2e8b76c3.nq.gz
│   └── repolex
│       └── fc351c5d6efd8dc2be7bb6cdc406412d2e8b76c3
│           └── chunk-001.nq.gz
├── blob
│   ├── 18785a0e6eb1ba283681003dbdaa402d15f867ff.nq.gz
│   ├── 1b763b1bae0d0061ad60e8847714df98e68f7eac.nq.gz
│   ├── 224ab849eff07ece72c822e23cd938657cea40f9.nq.gz
│   ├── 5585dc5fa5ac781ffddff8fc1cf3b496d1fabf61.nq.gz
│   ├── 5cb92a2d59531f0244a3a1d01dae835f67ad727e.nq.gz
│   ├── 610c2a54f1b57230de9b8c0cc7ac153344c10d19.nq.gz
│   ├── 61c533a22c3550569444dbfbecc492fb67f7d486.nq.gz
│   ├── 628ec286b4f434452336cccea57e1bd113fcbb9c.nq.gz
│   ├── 84be729e97500c3acad0b1acfd25e5855ef64a5f.nq.gz
│   ├── 92259e116ecb39fa2673daea3c0ebbeb85050d51.nq.gz
│   ├── 94f480de94e1d767531580401cbf13844868e82b.nq.gz
│   ├── d1b630276aae2dcf7a2e5f8b6b25de24db248bb2.nq.gz
│   ├── e066d41f968d010ad0c28831f4fe3c41a3b8041e.nq.gz
│   ├── e6950f57138cbdd93a302e6897a8047d5631c1b8.nq.gz
│   └── f3d4c1875d0c72ae60e8bb2bc93fb2866039ef0a.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── fc351c5d6efd8dc2be7bb6cdc406412d2e8b76c3.nq.gz
├── filetree
│   └── fc351c5d6efd8dc2be7bb6cdc406412d2e8b76c3.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 25 files
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

[princjef/commitlint-azure-pipelines-cli](https://github.com/princjef/commitlint-azure-pipelines-cli)

---
*Parsed on 2026-11-21 by [repolex](https://repolex.ai)*
