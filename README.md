# Repolex Knowledge Graph of Kozea/mandrill-api-python-3.7

RDF knowledge graph data for [Kozea/mandrill-api-python-3.7](https://github.com/Kozea/mandrill-api-python-3.7), parsed by [repolex](https://repolex.ai).

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
rlex download Kozea/mandrill-api-python-3.7
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 0ab4d9a992a782d1ddcfe2addee7e604be3236df
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 0ab4d9a992a782d1ddcfe2addee7e604be3236df
│           └── chunk-001.nq.gz
├── blob
│   ├── 1e0b5f8cfb715c17da9a0d57e66fd9014545dfe5.nq.gz
│   ├── 48387441f0a42271e0498c19d1f74c1991eb528f.nq.gz
│   ├── 4dda7128e1e117ed4865adc29fc6984a609ec824.nq.gz
│   ├── 73effa45c8a82d87a4c691f29e1065e655b7f126.nq.gz
│   ├── 79a373a2a73ec247d696344f5a9bfbfec4c4c781.nq.gz
│   ├── a9103adfe035ac88a696ed22b03a797329137943.nq.gz
│   ├── dfd048a002d2393dd1b92a978dba4faf00875448.nq.gz
│   ├── f4fbf578ddaf7e1620d85418e8031965a19d826c.nq.gz
│   ├── fa3bbc96f45ee2a9cd7fb28ad127955d85718735.nq.gz
│   └── fb922889739d28b2c3e40cbf010921c33735c577.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 0ab4d9a992a782d1ddcfe2addee7e604be3236df.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 17 files
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

[Kozea/mandrill-api-python-3.7](https://github.com/Kozea/mandrill-api-python-3.7)

---
*Parsed on 2026-10-28 by [repolex](https://repolex.ai)*
