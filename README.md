# Repolex Knowledge Graph of oconnor663/duct.rs

RDF knowledge graph data for [oconnor663/duct.rs](https://github.com/oconnor663/duct.rs), parsed by [repolex](https://repolex.ai).

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
rlex download oconnor663/duct.rs
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 9414b8ff719b4c1137e98368bb7f7051eea16295
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 9414b8ff719b4c1137e98368bb7f7051eea16295.nq.gz
│   └── repolex
│       └── 9414b8ff719b4c1137e98368bb7f7051eea16295
│           └── chunk-001.nq.gz
├── blob
│   ├── 041663399969d0c71048e13d5232616536927607.nq.gz
│   ├── 048b85ce597f04cc8108dfaa92428260188134ab.nq.gz
│   ├── 04f43b58e49169bcc1ecc64c7a8144e196c9ee46.nq.gz
│   ├── 079960bce7092c5336d22e06f1a7f002eb9f381d.nq.gz
│   ├── 1fdae05c9df7dd24f8a0fe27ab1011b0bebd3e79.nq.gz
│   ├── 2bf3a9e022c33e5ba0b86bd251d858f7a030fe09.nq.gz
│   ├── 38c24fd3c2a70ceae996faeacc1da2f5ae505106.nq.gz
│   ├── 3bfe801d207c1fde9831aeee944191efa5aae077.nq.gz
│   ├── 3eef415b1b0cc6c2b8ab0eacecd8bc9dcf81f8ab.nq.gz
│   ├── 4a373bf7a43468a01cd36dfc9c3145b35117995c.nq.gz
│   ├── 72dc60d84b692387206266939bc34656bcba1e15.nq.gz
│   ├── 952a4bc5724154012d4b67774381a9655a3c40f9.nq.gz
│   ├── 966ca5237f3ded22fd15ef34c46974cac8d47cdb.nq.gz
│   ├── 9ac2515b6e17df86ca26f5db82f9208bcbf3d6b1.nq.gz
│   ├── a0f1b7a6cea385489612f0df2971bf235b42f444.nq.gz
│   ├── a7dbccdcaeac812bded44dc63661d34588cffaa3.nq.gz
│   ├── a9d37c560c6ab8d4afbf47eda643e8c42e857716.nq.gz
│   ├── ace86bf9b0403e551ab4f5f6b51caad5c0d33607.nq.gz
│   ├── c7032809c37a40a1145772aff834739963981f7a.nq.gz
│   ├── c7f62ad83559df96565778ed6ffa1f3b084c4bf9.nq.gz
│   ├── c802a944224dafac0560d31ee3e5b09f0fa6bd5d.nq.gz
│   ├── e315615162cc3919f3596ebd54fa526ab31bd124.nq.gz
│   ├── ea5b60640b01f74e295037aa8a6b7d4ea278a739.nq.gz
│   └── f82748debaec633b76eeb7367d3ede032ffa8dcf.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 9414b8ff719b4c1137e98368bb7f7051eea16295.nq.gz
├── filetree
│   └── 9414b8ff719b4c1137e98368bb7f7051eea16295.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 34 files
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

[oconnor663/duct.rs](https://github.com/oconnor663/duct.rs)

---
*Parsed on 2026-11-22 by [repolex](https://repolex.ai)*
