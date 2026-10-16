# Repolex Knowledge Graph of xarray-contrib/xarray-schema

RDF knowledge graph data for [xarray-contrib/xarray-schema](https://github.com/xarray-contrib/xarray-schema), parsed by [repolex](https://repolex.ai).

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
rlex download xarray-contrib/xarray-schema
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── bed4d2d968922429c10b6594112b47b0f25dccd4
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── bed4d2d968922429c10b6594112b47b0f25dccd4
│           └── chunk-001.nq.gz
├── blob
│   ├── 05c5d2cc05f230a3ab1d3801c79c52f36e04e0ce.nq.gz
│   ├── 1dcc25ee5c41680fcfaf4d74b8cd94edb480ea91.nq.gz
│   ├── 2119f51099bf37e4fdb6071dce9f451ea44c62dd.nq.gz
│   ├── 28873d833f149d18cfd80816168836259b6b1011.nq.gz
│   ├── 36846b82a828a727810a4bd6713e5177f31da496.nq.gz
│   ├── 417e59fbf219028955be5fb5c68868fbbc243ee1.nq.gz
│   ├── 4a71e62adc8eb00774e9a793f6fde715e39faec3.nq.gz
│   ├── 4ab66a187879affd9d8cce605bd4ac0e5045123e.nq.gz
│   ├── 54b16a3f1e198b3200ef8ea50bc9b14cf1e51491.nq.gz
│   ├── 59afcd302d6a302245a4953705bc93ce62a28cfe.nq.gz
│   ├── 5aefb0eaca10771937f59a9d93039688f0d0eaba.nq.gz
│   ├── 688eca6fbb42fbab192a06e74c3929ccaadfcf71.nq.gz
│   ├── 6a0852a011592ae14f7c6ddbe8be461389ef1a06.nq.gz
│   ├── 73544fd2d0caa4275387d391c5374991763fbba4.nq.gz
│   ├── 86e6687d5d58fc05afc3993128ea8e08e13572a3.nq.gz
│   ├── 9010e521d04838232cc9129e037b634231c54b6f.nq.gz
│   ├── 97dd04f21a288446590cf39e191660f897f9dd20.nq.gz
│   ├── 9be35eee4e686d2c5cc9f90b321195528b823c47.nq.gz
│   ├── b5178a5f990be5836bf5e9282599dec62140d2a7.nq.gz
│   ├── bd76b89d924fd22fe938563772ebe5dbb2038dcc.nq.gz
│   ├── be81452d147689b59e3af1d068fa2cad1ae0cb51.nq.gz
│   ├── c198d46978365709cc92e48723c1601c99ba4dac.nq.gz
│   ├── cbe599f8f2f3d51cca09f7fc30f4b86ee46f6d4b.nq.gz
│   ├── cd4be04c487ad3b0c2f02d8f0b27629e4d563ce3.nq.gz
│   ├── d1ed565042bdda94e19e9e61904757443d1802f1.nq.gz
│   ├── d319bfee3c1798cbab42b6db91f94904100e78e1.nq.gz
│   ├── d4bb2cbb9eddb1bb1b4f366623044af8e4830919.nq.gz
│   ├── d881d6b6ae96411d5350d6de195f3d949b0f7022.nq.gz
│   ├── df71850dc7b52540644264444ee381a1bc79fe13.nq.gz
│   ├── e371fd42a28e4789c1b21cfc66ee32fa93d49d05.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   └── f07c1c5bb262e110a52c8eed9b556d420ce1f5ba.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── bed4d2d968922429c10b6594112b47b0f25dccd4.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 40 files
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

[xarray-contrib/xarray-schema](https://github.com/xarray-contrib/xarray-schema)

---
*Parsed on 2026-10-16 by [repolex](https://repolex.ai)*
