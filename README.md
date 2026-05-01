# Math MCP Server

A simple stdio MCP server built with [FastMCP](https://github.com/jlowin/fastmcp). Something for people to play with.

**Note:** This is a toy server! It exists just to get something up and running for testing/experimentation.

## Tools

| Tool | Description | Parameters |
|------|-------------|------------|
| `add` | Add two numbers | `a: int`, `b: int` → `int` |
| `multiply` | Multiply two numbers | `a: int`, `b: int` → `int` |

## Requirements

- Python >= 3.13
- [uv](https://docs.astral.sh/uv/) (recommended)

## Setup

```bash
uv sync
```

## Running the Server

```bash
uv run python server.py
```

The server uses `stdio` transport, so it is intended to be launched by an MCP client (e.g. Claude Desktop, Claude Code).

## Connecting to Claude Code

Add the server to your Claude Code MCP configuration:

```json
{
  "mcpServers": {
    "math": {
      "command": "uv",
      "args": ["run", "python", "/path/to/math-mcp/server.py"]
    }
  }
}
```

## License

MIT — see [LICENSE](LICENSE).
