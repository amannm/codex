# mcp-types

Types for Model Context Protocol. Inspired by https://crates.io/crates/lsp-types.

As documented on https://modelcontextprotocol.io/specification/2025-06-18/basic:

- TypeScript schema is the source of truth: https://github.com/modelcontextprotocol/modelcontextprotocol/blob/main/schema/2025-06-18/schema.ts
  -- JSON schema is amenable to automated tooling: https://github.com/modelcontextprotocol/modelcontextprotocol/blob/main/schema/2025-06-18/schema.json

## Regenerating the types

To update the generated Rust code in `src/lib.rs`, you need a Python interpreter (3.9+ is supported) and [uv](https://github.com/jayclassless/uv):

```bash
cd mcp-types
uv venv --cache-dir .uv-cache .venv
source .venv/bin/activate
python generate_mcp_types.py
```

This script no longer requires Python 3.10; it runs under Python 3.9 and above.
