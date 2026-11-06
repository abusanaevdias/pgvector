# pgvector — engineering notes

Vectors in PostgreSQL · Source review: 6 November 2026

## Purpose

A candidate when business records and embeddings should share PostgreSQL transactions and relational filtering.

## Architecture reviewed

A PostgreSQL extension for exact and approximate vector similarity search; SQL, C source and tests are kept together.

Repository areas inspected: `src, sql, test, vector.control` (root inventory and linked README documentation).

## Decision and trade-off

Choose distance and indexes to match the embedding model; approximate search needs recall/latency measurement on the actual corpus.

## Verification to perform

Compare approximate results against exact search; test filtered recall; verify an index migration on disposable data.

This is a source review and a proposed verification plan. No upstream runtime suite, deployment, provider benchmark or paid API evaluation was run for these notes.

## Attribution and scope

- Original project: [pgvector/pgvector](https://github.com/pgvector/pgvector).
- Original license: PostgreSQL-style license (see retained LICENSE); retained without replacement.
- Original README and source history remain part of the fork.
- This portfolio layer adds documentation; it does not claim authorship of the upstream project or an accepted upstream contribution.
- Dependency licenses, model weights, hosted services and any existing NOTICE files remain subject to their own terms.

## Start from the maintained instructions

Read the [upstream README](https://github.com/pgvector/pgvector/blob/master/README.md) and its contribution guidance for current installation and development commands.
