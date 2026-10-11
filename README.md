# Repolex Knowledge Graph of litestar-org/fast-query-parsers

RDF knowledge graph data for [litestar-org/fast-query-parsers](https://github.com/litestar-org/fast-query-parsers), parsed by [repolex](https://repolex.ai).

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
rlex download litestar-org/fast-query-parsers
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 625a2d1f9893a8350dcd0b4f95e619f83697a7e3
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 625a2d1f9893a8350dcd0b4f95e619f83697a7e3
│           └── chunk-001.nq.gz
├── blob
│   ├── 03a6d327f1b9cd68ceb67b938bb3cd5b6f064745.nq.gz
│   ├── 0475124bb4eac91e3ef794026f17b86315e8671e.nq.gz
│   ├── 0a7c8b29cbe0db0bea112b4b5bb9ee9693516a0e.nq.gz
│   ├── 123014908bebbfb7ecfa1d15daaceb272fabe05b.nq.gz
│   ├── 128b1334636b358da30ead072d709c4c78a2a33c.nq.gz
│   ├── 160864063b2e751630ac47a81a9d4daa49f78dfe.nq.gz
│   ├── 2726854b10550e52dc1d6365b87e3b2d07956984.nq.gz
│   ├── 305d680de7d86f047f49381090698f2083a5b9bf.nq.gz
│   ├── 419898b97de4c8bf33fcfc8444df9464c34d4352.nq.gz
│   ├── 47526163d346f79ea0084b7ce1df53eb06d3fe98.nq.gz
│   ├── 526b19edb0d8aea43ccc39b661d8d79bb2b8bb4d.nq.gz
│   ├── 535bb9a7c5987bc130dd609541a944a76a95f609.nq.gz
│   ├── 57ab360958743d0365176c5c98ca2c95dd0232e2.nq.gz
│   ├── 6c8621c20387c2ef65518075d06114944340dd28.nq.gz
│   ├── 8700604b3cf4e581a670d08896ce855d635b487f.nq.gz
│   ├── a09ef6b457ac99515b8a3dba7119fb47c2d68710.nq.gz
│   ├── b0940f1a0c17b27f3a89b5e940d7cf652e430896.nq.gz
│   ├── c575f84fe6cc7455a02279c365822033ef4a4955.nq.gz
│   ├── cd24307e1302fd5a1ed852b9be3e2fc16db1becc.nq.gz
│   ├── ddd8141f019e86b41cbafeb0e72f79bb5e4023ab.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   └── fcabfcd7781899d9f746c8708d71125f243474d4.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 625a2d1f9893a8350dcd0b4f95e619f83697a7e3.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 30 files
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

[litestar-org/fast-query-parsers](https://github.com/litestar-org/fast-query-parsers)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
