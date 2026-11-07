# Repolex Knowledge Graph of sunpy/sunpy-contribution-statistics

RDF knowledge graph data for [sunpy/sunpy-contribution-statistics](https://github.com/sunpy/sunpy-contribution-statistics), parsed by [repolex](https://repolex.ai).

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
rlex download sunpy/sunpy-contribution-statistics
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── aef818ebe504b38cf7e183850faad39feeedb49e
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── aef818ebe504b38cf7e183850faad39feeedb49e
│           └── chunk-001.nq.gz
├── blob
│   ├── 13b7a939e604292f4f623a0e124c491da5590910.nq.gz
│   ├── 152052f6852f9b3e710244503fbcf8a990c05d18.nq.gz
│   ├── 1547761a83f5d4b214a656039bd1f99936847019.nq.gz
│   ├── 1a218f5e5bc6f6fcf957402a14d721e762095351.nq.gz
│   ├── 1ae3f8f644a24077ac3a4d3c77344974475e6d17.nq.gz
│   ├── 1e828e0e346ef0c44bb76f8248f95e04faa00fa2.nq.gz
│   ├── 2119f51099bf37e4fdb6071dce9f451ea44c62dd.nq.gz
│   ├── 25183d00d89ed4d8e52378cb11cdaab5238c2b1e.nq.gz
│   ├── 4c30051dcee22de48cc11f87a0fc20d194edfdd2.nq.gz
│   ├── 5531875b1fec1d3f1f5e85dd69c0b5b2ed95ccc2.nq.gz
│   ├── 61a63c5501efef5083fdc9ad1c14503b812c9d5f.nq.gz
│   ├── 79d4aabc1c508577eba052c8f83150d68a808cdd.nq.gz
│   ├── 851940cb136b9c9d81e0df9e3cbbfbfaf46abdfe.nq.gz
│   ├── a50ed861ba00e674fb0a05566c955898065f81f4.nq.gz
│   ├── b7a660821c842b9829c646a7d512816dc8b4f4d6.nq.gz
│   ├── b80e9825e5617cf6dbe476f10ba46a16d5119d60.nq.gz
│   ├── c86ec4a28b6bc3bdb442622245ab9bab9e416eb0.nq.gz
│   ├── cdf8630280e37a7e8040dd5a32e3c13a9794e6d4.nq.gz
│   ├── d4bb2cbb9eddb1bb1b4f366623044af8e4830919.nq.gz
│   ├── d94f4034f0ffbab993b8319af5ecffe9d2602468.nq.gz
│   ├── ea07ca2ae2e6307daa93009b42b08c1d54955871.nq.gz
│   ├── ed285f170871a3b0a93bb5f2be6ee7827f2d352c.nq.gz
│   ├── f04b60d010f6f85d055931cc30cd11ff5bc05d94.nq.gz
│   ├── f0fce1df9f02ed66f7761c52aa9272257931d5a3.nq.gz
│   ├── f102a9cadfa89ce554b3b26d2b90bfba2e05273c.nq.gz
│   ├── f2008a2181eb83d7c87ab76fe72fc8006cb1edaf.nq.gz
│   └── f80d9c4340d359e74aa3066cad1bac66ac7e6a4a.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── aef818ebe504b38cf7e183850faad39feeedb49e.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 35 files
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

[sunpy/sunpy-contribution-statistics](https://github.com/sunpy/sunpy-contribution-statistics)

---
*Parsed on 2026-11-07 by [repolex](https://repolex.ai)*
