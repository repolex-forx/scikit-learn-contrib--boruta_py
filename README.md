# Repolex Knowledge Graph of scikit-learn-contrib/boruta_py

RDF knowledge graph data for [scikit-learn-contrib/boruta_py](https://github.com/scikit-learn-contrib/boruta_py), parsed by [repolex](https://repolex.ai).

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
rlex download scikit-learn-contrib/boruta_py
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── dd7b020cdc23c98fe908c14771cbf931dc8b7e62
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── dd7b020cdc23c98fe908c14771cbf931dc8b7e62
│           └── chunk-001.nq.gz
├── blob
│   ├── 0486d0ec58a10e3b8c7586ac8fca48dc62f8485e.nq.gz
│   ├── 29e70318e88059f1d75e39350cb67bc98b08b625.nq.gz
│   ├── 38d1112de7fcceb78dea8981e93b7f87bc781232.nq.gz
│   ├── 4160bb0a715c0ddc6f5ab3b861bb3b7622f98a99.nq.gz
│   ├── 45abf2d97a5aa2b3004db7e47111ec6dbd9a5664.nq.gz
│   ├── 64a36913c12ff81a237bf337e48aecf70f9bf15f.nq.gz
│   ├── 8d9ea4529562501db5887b44b12568ed8dc8cc8d.nq.gz
│   ├── b7da0d9eb762bc3d3c91a080e47f63e3a63d0f5b.nq.gz
│   ├── c241e2015be1716a875974499b20b2ec13a0433a.nq.gz
│   ├── d2a2d0a95e6adf3cf9ce1fd57609e3019e2a6f07.nq.gz
│   ├── d8430e593725e89821b61b4bde907c555f0c2092.nq.gz
│   ├── e22d5f149b24548fdda08b6806a3394f0907158f.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   └── eedc6fd18f06a32282d3280a1c022e13a6c50228.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── dd7b020cdc23c98fe908c14771cbf931dc8b7e62.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 22 files
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

[scikit-learn-contrib/boruta_py](https://github.com/scikit-learn-contrib/boruta_py)

---
*Parsed on 2026-10-15 by [repolex](https://repolex.ai)*
