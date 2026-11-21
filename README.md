# Repolex Knowledge Graph of abonander/mime_guess

RDF knowledge graph data for [abonander/mime_guess](https://github.com/abonander/mime_guess), parsed by [repolex](https://repolex.ai).

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
rlex download abonander/mime_guess
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 27de5609c1f916fd394d4e22c298f97d724dd26a
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 27de5609c1f916fd394d4e22c298f97d724dd26a.nq.gz
│   └── repolex
│       └── 27de5609c1f916fd394d4e22c298f97d724dd26a
│           └── chunk-001.nq.gz
├── blob
│   ├── 2294fcb5b6abac1c4129264cd8527898505f0595.nq.gz
│   ├── 2e18221000e81e0ee52f173a3343087a342152cc.nq.gz
│   ├── 4aa2fd1e4d48b7f3d2702367ce47d4e746f3bb3f.nq.gz
│   ├── 506260287f1e1dcb0d66fa599e1d357addce4bb9.nq.gz
│   ├── 6ab44adb4842d46130c0f40d99dba49ab55d5dcb.nq.gz
│   ├── 9542ff008ee6fef4cfe8b716e4d2c19624a5f789.nq.gz
│   ├── c5350bd24faf9eafc88ab00b3dceb2275077e534.nq.gz
│   ├── d35bada1477e16af4f5db5fc4c6a71e42c4668f2.nq.gz
│   ├── d90db9584417b52827ad06c1ec8c327759def3e4.nq.gz
│   ├── e2f5e1bcfe28299efd0704a3f3c9bd6578ea66d6.nq.gz
│   └── e3a186285799d19d6773b8c219b45b290d94aca1.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 27de5609c1f916fd394d4e22c298f97d724dd26a.nq.gz
├── filetree
│   └── 27de5609c1f916fd394d4e22c298f97d724dd26a.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 21 files
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

[abonander/mime_guess](https://github.com/abonander/mime_guess)

---
*Parsed on 2026-11-21 by [repolex](https://repolex.ai)*
