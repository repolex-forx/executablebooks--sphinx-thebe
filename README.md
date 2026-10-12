# Repolex Knowledge Graph of executablebooks/sphinx-thebe

RDF knowledge graph data for [executablebooks/sphinx-thebe](https://github.com/executablebooks/sphinx-thebe), parsed by [repolex](https://repolex.ai).

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
rlex download executablebooks/sphinx-thebe
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 60aa219f0a69939337510776b12fb3e54c444454
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 60aa219f0a69939337510776b12fb3e54c444454
│           └── chunk-001.nq.gz
├── blob
│   ├── 13252d22ef1fe74bd182348d1782d7a89bc49d98.nq.gz
│   ├── 1c8d1ab9c972229a3fbc504d49f626c6a3f1cc22.nq.gz
│   ├── 1da27930c257319b15b754b41576d7b8b0afbe67.nq.gz
│   ├── 481dbcad1c977aa7207b2535c7c160632c0cc415.nq.gz
│   ├── 4e491bb0e7e18fc21c2b6a29b6930b8c2b349a8e.nq.gz
│   ├── 67055804c23e04fceb5a8e378f383000c01b3843.nq.gz
│   ├── 6fd486de397922a0f32a40a6cc9525afb4ef81a4.nq.gz
│   ├── 8261b353e8cb01273fad0ba8573b66cfc72e8d5c.nq.gz
│   ├── 8fb235d7045be0330d94bcb3abd2ac43badaa197.nq.gz
│   ├── 951baec2e7542c8b9e73343b4d55e196550d4570.nq.gz
│   ├── 9d50ff17569a7bf7166a183ae2b72475adcfba09.nq.gz
│   ├── af278b9b7444c0de1da68bf8d9673937988d212d.nq.gz
│   ├── bb6ad31f28e51f73a3bccb67773251ff14af2f47.nq.gz
│   ├── bcd81f7a6d11914d9173c2452869209130f1f6cc.nq.gz
│   ├── c5410ec16606021577cb0b1adbcefda792504273.nq.gz
│   ├── c818922825cd112a24906862879a8986baa15200.nq.gz
│   ├── c875455cf7149771db3bd0a6954fa7d539a91d86.nq.gz
│   ├── cd126252cb9fd9236178b5270addb721f56b5d16.nq.gz
│   ├── d6e946149293b952e4b5ce151c2b4666a84d4fa0.nq.gz
│   ├── d92b1d3b177aad0451488195cd6c544fd0e1f66a.nq.gz
│   ├── dab6ba48f3dcb26eae65920afb84113b1ebb141f.nq.gz
│   ├── e0074aa34e987476a214065f5532b302f0613e6f.nq.gz
│   ├── e9983f58a89f39481d3d1e3f6d9eb44be2e08b53.nq.gz
│   └── f85c18946c01b35af153c3f5ca88b63523b1e09f.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 60aa219f0a69939337510776b12fb3e54c444454.nq.gz
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

[executablebooks/sphinx-thebe](https://github.com/executablebooks/sphinx-thebe)

---
*Parsed on 2026-10-12 by [repolex](https://repolex.ai)*
