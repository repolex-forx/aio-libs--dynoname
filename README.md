# Repolex Knowledge Graph of aio-libs/dynoname

RDF knowledge graph data for [aio-libs/dynoname](https://github.com/aio-libs/dynoname), parsed by [repolex](https://repolex.ai).

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
rlex download aio-libs/dynoname
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 92a80b5ad5797ad78f214ec78e0ddec50a5ea557
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 92a80b5ad5797ad78f214ec78e0ddec50a5ea557
│           └── chunk-001.nq.gz
├── blob
│   ├── 0236c92865866a7368323047641148780ec5371e.nq.gz
│   ├── 0b2f7b0655f41276d418ca8302dbaec8b7e7e829.nq.gz
│   ├── 21933bc4fce1365226b4200f5cc6205e4314899f.nq.gz
│   ├── 40eca1b6eae44ad0e94514cf566811dbf9ce9b33.nq.gz
│   ├── 486dece5ff6267b16e926be40f897c9dca47de6a.nq.gz
│   ├── 70c83212dac27916184044c2aecea7332742d321.nq.gz
│   ├── 8d7198c175e2c740cfe07bb0cdbe61c3567324c9.nq.gz
│   ├── 8fdcba4540ca996e110a2517e81b8d6e43067d8b.nq.gz
│   ├── a4ea92737fc4dcd5f3a9b8bbd85da573db195ad6.nq.gz
│   ├── b5807494c4766e9e8b46c90a802fe1c0e63b1208.nq.gz
│   ├── ccb4236bd2b9c36391025034d26cbe30a1c6ff52.nq.gz
│   ├── d1f709c9e63f4b70cbe729078fc140de207362c7.nq.gz
│   ├── d99cc94fc3c325fde9db01e949a975118f5a7a55.nq.gz
│   └── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 92a80b5ad5797ad78f214ec78e0ddec50a5ea557.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 21 files
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

[aio-libs/dynoname](https://github.com/aio-libs/dynoname)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
