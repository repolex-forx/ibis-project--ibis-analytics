# Repolex Knowledge Graph of ibis-project/ibis-analytics

RDF knowledge graph data for [ibis-project/ibis-analytics](https://github.com/ibis-project/ibis-analytics), parsed by [repolex](https://repolex.ai).

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
rlex download ibis-project/ibis-analytics
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── cfbf6a2a232c67eeabc60b5584b9ca0bd7544243
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── cfbf6a2a232c67eeabc60b5584b9ca0bd7544243
│           └── chunk-001.nq.gz
├── blob
│   ├── 00a1c4d4437e1c4769175e5d4b64493845dede89.nq.gz
│   ├── 075b2542afb820ca0c990f02a196dfbb35c41a3a.nq.gz
│   ├── 3ada19975a279a3d2db9303726851491dfaf9540.nq.gz
│   ├── 40b6ae6be4bb6e8f4c94cd17e49e50407bb65f13.nq.gz
│   ├── 441a6cf9662b3a381f78815353ab7fa83e27dc3b.nq.gz
│   ├── 44e60129501bc290237fd91015ef7b61a19d061f.nq.gz
│   ├── 461ef413d0dcac3ac6b6eb52c207c3ae6fb2b287.nq.gz
│   ├── 49b9599c97d9e27211e1dfcdf033d3c484580e76.nq.gz
│   ├── 6f98da1ddbf8328266414d3ac457c8b848420385.nq.gz
│   ├── 7545bd1e88e5842eca394190382395b37a7f1ad7.nq.gz
│   ├── 7dfd25b12f92252cde65c8a30dd53ba980d53537.nq.gz
│   ├── 7fecd2810c9b436195389ff56a03738606942365.nq.gz
│   ├── 8b137891791fe96927ad78e64b0aad7bded08bdc.nq.gz
│   ├── a03a6b54bfc34121df9134d7708f195c22c053d1.nq.gz
│   ├── b514dd3304e1263f128d2ae64259eeb569370cec.nq.gz
│   ├── be16b23185aa48dc62ed196780fd675221b08d55.nq.gz
│   ├── be872e2dcefad94154e42b6e9c222ee65458fb1e.nq.gz
│   ├── c2e2159276a469da9205b21926c6f0f425edaf0f.nq.gz
│   ├── c7563debfe221197929f50d706bedd9f5064917d.nq.gz
│   ├── c8e72960f94d1670a80df27373e9e17e2a510f9a.nq.gz
│   ├── ca978196de2253d6e68af15f1293e8bea1e1a3af.nq.gz
│   ├── cbf979c707d465d957fabeedf6b988c2f606b1fd.nq.gz
│   ├── cdeb599acc9b2dd28a6e41cd4731a83bfda20447.nq.gz
│   ├── ce01843e18dd237d828eaf8f60eacce4cc04fc14.nq.gz
│   ├── d806488cb7c5f0ea630554c97b1607e554c22690.nq.gz
│   ├── e33a42c0173b7afac9236a86903e56d4b9251184.nq.gz
│   ├── e4f721cd5cc1acb37955f0162243259c3095bed2.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── eded458cf208b3be0aa2fba0e2c33cae5c517548.nq.gz
│   └── fa5cdec312917e10ab7a80ba299b94d2863f8731.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── cfbf6a2a232c67eeabc60b5584b9ca0bd7544243.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 38 files
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

[ibis-project/ibis-analytics](https://github.com/ibis-project/ibis-analytics)

---
*Parsed on 2026-10-21 by [repolex](https://repolex.ai)*
