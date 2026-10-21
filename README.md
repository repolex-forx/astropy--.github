# Repolex Knowledge Graph of astropy/.github

RDF knowledge graph data for [astropy/.github](https://github.com/astropy/.github), parsed by [repolex](https://repolex.ai).

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
rlex download astropy/.github
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 69b634e2ebbec34e74160a298365d74ad04399ac
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 69b634e2ebbec34e74160a298365d74ad04399ac
│           └── chunk-001.nq.gz
├── blob
│   ├── 0158aa4e6d23676024ac3b76ece6f90a0254c799.nq.gz
│   ├── 0536b0b1470dd1f9eb2956049f30f6985b1e3bdb.nq.gz
│   ├── 114f74612bae3f890672e60a0ade529d6a9c9f01.nq.gz
│   ├── 248f97cea442e8b209d0b778f4f8ffba4ab125ab.nq.gz
│   ├── 26eae3733cc58eb657b37c79cd4351bdb56ae56e.nq.gz
│   ├── 4c2a1cc4091dd4b935092b2b0820204a13d011a9.nq.gz
│   ├── 77d5bd63c184f9a70959ef75676ba6824fc33832.nq.gz
│   ├── 9bf662424dc00f978bc986cc4d93b81ee2d1c0a5.nq.gz
│   └── c18dd8d83ceed1806b50b0aaa46beb7e335fff13.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 69b634e2ebbec34e74160a298365d74ad04399ac.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 17 files
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

[astropy/.github](https://github.com/astropy/.github)

---
*Parsed on 2026-10-21 by [repolex](https://repolex.ai)*
