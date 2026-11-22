# Repolex Knowledge Graph of ramosbugs/oauth2-rs

RDF knowledge graph data for [ramosbugs/oauth2-rs](https://github.com/ramosbugs/oauth2-rs), parsed by [repolex](https://repolex.ai).

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
rlex download ramosbugs/oauth2-rs
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 72ce74401c26eb4dc85dcbfde587bbcfc149e3ae
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 72ce74401c26eb4dc85dcbfde587bbcfc149e3ae.nq.gz
│   └── repolex
│       └── 72ce74401c26eb4dc85dcbfde587bbcfc149e3ae
│           └── chunk-001.nq.gz
├── blob
│   ├── 038e6c1a3be8fefcbf2b9765fd0bd9307abf4cbe.nq.gz
│   ├── 039bfa5eb10f953d2478017483492c4f84d1ebba.nq.gz
│   ├── 105f764b9fd0f590a37379b4ed49297ff2b07343.nq.gz
│   ├── 16fe87b06e802f094b3fbb0894b137bca2b16ef1.nq.gz
│   ├── 1a7bbf66cc6b25786c99d495584a641c7ada82ff.nq.gz
│   ├── 1ec99c8f4b04a1fa2d96f6bfbb1017f90c7489a7.nq.gz
│   ├── 2e562585f5eed5c82110e0634e95a2f902633c58.nq.gz
│   ├── 3254cb034caedf499d15a080acadb5bcbb190998.nq.gz
│   ├── 33f2df3ea280c1f37a1888d27e64d78f5890e633.nq.gz
│   ├── 35842d1926d3377c4b1b037d1a420563782171d8.nq.gz
│   ├── 39e0ed6602151f235148e6c08413aa7eda5b9038.nq.gz
│   ├── 3b0c857f48152c110a6aa51bbb2443b84a949f26.nq.gz
│   ├── 401f49b72836fdad2ac8ce3cd0742ae7a43dda70.nq.gz
│   ├── 43b7731f5b80c231efc12ea5cb75b63173274959.nq.gz
│   ├── 543dcc22c3bd4c6cec9ab43b02744067d941881a.nq.gz
│   ├── 5c66d57ea7c117efd600987f5d6102876f89d86a.nq.gz
│   ├── 6948bb17eaa4ff25dd6ed335200f887f021d3d80.nq.gz
│   ├── 6d3bf1f99cb926f5e1b1b6d71145aa2b7d07fdd1.nq.gz
│   ├── 7ec702eaa9ea94ce2caf7f5ce16c9f4dd08d6a84.nq.gz
│   ├── 96f987c22fdd909fe884c7473c204d60ee2897c4.nq.gz
│   ├── 97f8aac7a8d90ed319cb2307b2a7231bdcd25131.nq.gz
│   ├── 98e01e5ac4c8dcdf90b20b47e7edb0c1422fd293.nq.gz
│   ├── 99ff52b506a7ff51e04db28ad1f5c6d523f66ebf.nq.gz
│   ├── a40166fa860b4b3ba2146ff220d9e9b1e88f7ba1.nq.gz
│   ├── a46772f752200fceb6a97e44970121d62174044a.nq.gz
│   ├── a5943df90570974f6d5a221def191f345710a1b1.nq.gz
│   ├── aa23b1eaad07283ae2f17ea9fde5fd9b466ad2e7.nq.gz
│   ├── aa5787475f506d8763eb9ee50b1088dd01dcb0f5.nq.gz
│   ├── b90c413b6f81d9ef69440692144d836a0fb64bbd.nq.gz
│   ├── bc51dce09ff0d795e27a1894f606824d277ab66e.nq.gz
│   ├── c5bd8e8c139ae5c08880d9712c2ee7cd524178a2.nq.gz
│   ├── c684f5244beeb2436af30b3b91faea5dacd6924f.nq.gz
│   ├── d3dba53745d8209a37c262956d4a0bc0016ee282.nq.gz
│   ├── d93d80be05faa1b33b8f159b05cc28359ec26ea5.nq.gz
│   ├── e148942cddb540da2a36c9787ecb4bc91dca8cf2.nq.gz
│   ├── eccfd1dd6abcfa3e7f1a98ff45329c8586ea56ac.nq.gz
│   ├── fc17e3cc1360cbe38509c87096aabc63775f531f.nq.gz
│   └── fe960f2ed0a198bfb24d63ff921145a518f17086.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 72ce74401c26eb4dc85dcbfde587bbcfc149e3ae.nq.gz
├── filetree
│   └── 72ce74401c26eb4dc85dcbfde587bbcfc149e3ae.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 48 files
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

[ramosbugs/oauth2-rs](https://github.com/ramosbugs/oauth2-rs)

---
*Parsed on 2026-11-22 by [repolex](https://repolex.ai)*
