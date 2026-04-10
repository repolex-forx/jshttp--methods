# Repolex Knowledge Graph of jshttp/methods

RDF knowledge graph data for [jshttp/methods](https://github.com/jshttp/methods), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [lexq](https://github.com/repolex-ai/lexq) query tool using [uv](https://docs.astral.sh/uv/getting-started/installation/).

If you have uv installed, just copy/paste this into your terminal:

```bash
uv tool install git+https://github.com/repolex-ai/lexq
```

This installs lexq onto your system, in your user context. Verify the install:

```bash
lexq --help
```

**lexq is designed to be used primarily by LLMs in a terminal.** Start up your favorite LLM and ask it to use the lexq tool. It's that easy!

To load this repo's data:

```bash
lexq download jshttp/methods
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 25d257d913f1b94bd2d73581521ff72c81469140
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 25d257d913f1b94bd2d73581521ff72c81469140.nq.gz
│   └── repolex
│       └── 25d257d913f1b94bd2d73581521ff72c81469140
│           └── chunk-001.nq.gz
├── blob
│   ├── 220dc1a247943ef3837b65754455dfb179260070.nq.gz
│   ├── 2c727d4600cdc38628cf814a588b5ec82d0fcd84.nq.gz
│   ├── 2fd752c632e1736007337ce39108c042cb8c2f0c.nq.gz
│   ├── 527beaba83a9e7e8cae815634c4448e8347782c3.nq.gz
│   ├── 667a50bde7d852359b1ebd9fa8ea8b8582bc64ac.nq.gz
│   ├── 672a32bfe5d685306f18b7a81a15af9fbbd00a0f.nq.gz
│   ├── c0ecf072db3f9809c46c83f5641b5df99c686bbf.nq.gz
│   ├── c4ce6f053c68581068898fd2a4be53a861e5b1b5.nq.gz
│   └── e4e8965236c6c42541e4c9e2d72d30196d3f8f80.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 25d257d913f1b94bd2d73581521ff72c81469140.nq.gz
├── filetree
│   └── 25d257d913f1b94bd2d73581521ff72c81469140.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 19 files
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

## Source repository

[jshttp/methods](https://github.com/jshttp/methods)

---
*Parsed on 2026-04-10 by [repolex](https://repolex.ai)*
