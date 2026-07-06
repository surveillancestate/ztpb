# ztpb

Zig, TypeScript, PostgreSQL, Bun.

A small stack for building web products with native systems components.

## Stack

```txt
Zig        systems code, native tools, agents, CLIs
TypeScript application code, shared types, UI logic
PostgreSQL durable state, queries, audit trails
Bun        runtime, server, tooling, tests, builds
```

## Why

The goal is to keep the stack small while still covering the full product surface:

```txt
web apps
APIs
workers
native binaries
local agents
database-backed workflows
internal tools
```

TypeScript and Bun handle the product layer.

PostgreSQL is the source of truth.

Zig is used when code needs to touch the OS, files, processes, networking, or performance-sensitive boundaries.

## Repo shape

```txt
ztpb/
  apps/
    web/
    api/
    admin/

  packages/
    core/
    db/
    ui/

  engines/
    agent/
    net/
    files/
    ipc/

  sql/
    migrations/
    seeds/

  scripts/
```

## Guidelines

Use TypeScript for application and product logic.

Use Zig for native/system code.

Use PostgreSQL for durable state, auditability, queues, and reporting.

Use Bun for running, building, testing, and scripting.

Avoid adding infrastructure until the stack actually needs it.

## Notes

This repo is a place to collect reusable patterns, modules, and examples for the ZTPB stack.
