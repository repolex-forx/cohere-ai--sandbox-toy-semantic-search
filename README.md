# Repolex Knowledge Graph of cohere-ai/sandbox-toy-semantic-search

RDF knowledge graph data for [cohere-ai/sandbox-toy-semantic-search](https://github.com/cohere-ai/sandbox-toy-semantic-search), parsed by [repolex](https://repolex.ai).

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
rlex download cohere-ai/sandbox-toy-semantic-search
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── c27c9174c950d58e8c6ee0e6f49fc9a2cc414a5b
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── c27c9174c950d58e8c6ee0e6f49fc9a2cc414a5b
│           └── chunk-001.nq.gz
├── blob
│   ├── 0fa0fae5b5a2ffd25bc4c930245da3a6f243cbad.nq.gz
│   ├── 14078e64b2be653240c655412e7838c972090c26.nq.gz
│   ├── 191cf4e7b095f7c74d52f3da8952b3e341b290d7.nq.gz
│   ├── 27b3bde82c754284b05a693be07efd2344e9be52.nq.gz
│   ├── 28d68763aae69d0766bdc222a8610c87cf9c3976.nq.gz
│   ├── 2b2af20b7a73bc514631bd0d50a340c004b9bafd.nq.gz
│   ├── 342d26f46014dde74fc58a42c071dd22efe9b568.nq.gz
│   ├── 45ce1f6497342bf6666af140569723a000f64f54.nq.gz
│   ├── 484fdad55d233695528ee79b49f00a9fbc4b116b.nq.gz
│   ├── 4e69de2be1df73071bb03d535fa03841e840dbb0.nq.gz
│   ├── 59830a042d5ac96aa4e755b1991fa03c6ef0ea83.nq.gz
│   ├── 72aaa1596edefcbf7d10fd4f7ebf878f3fe99221.nq.gz
│   ├── 7759b19a0ce0fb7a8fc74df5147f9cdde30c008b.nq.gz
│   ├── 79760155d867508425d4d887923d0d5ba211a497.nq.gz
│   ├── 9070ad2c24474a41e6e09158a1369eb6d77d7cc5.nq.gz
│   ├── b78d90a26a15600d813d5c2c77871029d2fb2e3a.nq.gz
│   ├── be95eb0df339be149843bfcfcec3dae54bcc16ca.nq.gz
│   ├── bf67ae59ed81dc591d7a39031374c843f88b2d04.nq.gz
│   ├── bf9aa7cb07a1c7f63f2a18759b4d6e372e5e7c6f.nq.gz
│   ├── cec0a63c1586071d2cf2ba8818ac4dcb0ed82dd5.nq.gz
│   ├── d6aa47f622dbe6160fe782e55b4ae96040b61746.nq.gz
│   ├── e02b86a4a1685252ef596dbdfc6aad67d03c0761.nq.gz
│   ├── e6a4c4763d87889973d166b8fbe6a8aeaad103bf.nq.gz
│   └── ed2de590d35e9b764b1fd25d5d669ca3ed22a68b.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── c27c9174c950d58e8c6ee0e6f49fc9a2cc414a5b.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 32 files
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

[cohere-ai/sandbox-toy-semantic-search](https://github.com/cohere-ai/sandbox-toy-semantic-search)

---
*Parsed on 2026-11-08 by [repolex](https://repolex.ai)*
