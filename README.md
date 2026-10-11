# Repolex Knowledge Graph of pytest-dev/pytest-instafail

RDF knowledge graph data for [pytest-dev/pytest-instafail](https://github.com/pytest-dev/pytest-instafail), parsed by [repolex](https://repolex.ai).

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
rlex download pytest-dev/pytest-instafail
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── fcf1413418fa3b049d87b9f750ba8b2b5a480d39
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── fcf1413418fa3b049d87b9f750ba8b2b5a480d39
│           └── chunk-001.nq.gz
├── blob
│   ├── 08d3803c2c27d138e8b42afb1dcb3548993f3d72.nq.gz
│   ├── 40c9126aeb34a7001fcf3823b2ed5e2791b8c68f.nq.gz
│   ├── 6180cc53cec9fdd7e9f72c58d41284052bd8858a.nq.gz
│   ├── 7221a156deabc733106c465e8639c23806660ddb.nq.gz
│   ├── 7b8666629e5f268c0f1c34863706b3d1a933ea01.nq.gz
│   ├── 9562b6818122bc3e987b9a83adfdb5245a3dc3ea.nq.gz
│   ├── c552774295fefa611abd1518d42e8377843a994d.nq.gz
│   ├── d24941a6a6ef3b808e39a7596e7434acbfc457d9.nq.gz
│   ├── d8ae90c7109494332c96d423351a8531aec412b8.nq.gz
│   ├── fbabd8d4bd61acb6b00c51936d4092ff33a937f1.nq.gz
│   └── fcf7fd8d948a9bfbbac66c64c019405cf067b4d1.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── fcf1413418fa3b049d87b9f750ba8b2b5a480d39.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 19 files
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

[pytest-dev/pytest-instafail](https://github.com/pytest-dev/pytest-instafail)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
