<p align="center">
  <h1>Strands Agents MCP Server</h1>
</p>

<div align="center">
  <a href="https://github.com/strands-agents/mcp-server/graphs/commit-activity"><img alt="GitHub commit activity" src="https://img.shields.io/github/commit-activity/m/strands-agents/mcp-server"/></a>
  <a href="https://github.com/strands-agents/mcp-server/issues"><img alt="GitHub open issues" src="https://img.shields.io/github/issues/strands-agents/mcp-server"/></a>
  <a href="https://github.com/strands-agents/mcp-server/blob/main/LICENSE"><img alt="License" src="https://img.shields.io/github/license/strands-agents/mcp-server"/></a>
  <a href="https://pypi.org/project/strands-agents-mcp-server/"><img alt="PyPI version" src="https://img.shields.io/pypi/v/strands-agents-mcp-server"/></a>
  <a href="https://python.org"><img alt="Python versions" src="https://img.shields.io/pypi/pyversions/strands-agents-mcp-server"/></a>
</div>

<div>
This MCP server provides documentation about Strands Agents,
so you can use your favorite AI coding assistant to vibe-code AI agents
with the Strands Agents SDK.
</div>

## Installation

You can use the Strands Agents MCP server with
[40+ applications that support MCP servers](https://modelcontextprotocol.io/clients),
including Amazon Q Developer CLI, Anthropic Claude Code, Cline, and Cursor.

### Q Developer CLI example

See the [Q Developer CLI documentation](https://docs.aws.amazon.com/amazonq/latest/qdeveloper-ug/command-line-mcp-configuration.html)
for instructions on managing MCP configuration.

In `~/.aws/amazonq/mcp.json`:

```json
{
  "mcpServers": {
    "strands": {
      "command": "uvx",
      "args": ["strands-agents-mcp-server"]
    }
  }
}
```

### Claude Code example

See the [Claude Code documentation](https://docs.anthropic.com/en/docs/claude-code/tutorials#configure-mcp-servers)
for instructions on managing MCP servers.

```bash
claude mcp add strands uvx strands-agents-mcp-server
```

### Cline example

See the [Cline documentation](https://docs.cline.bot/mcp-servers/configuring-mcp-servers#editing-mcp-settings-files)
for instructions on managing MCP configuration.

Provide Cline with the following information:

```
I want to add the MCP server for Strands Agents.
Here's the GitHub link: @https://github.com/strands-agents/mcp-server
Can you add it?"
```

### Cursor example

See the [Cursor documentation](https://docs.cursor.com/context/model-context-protocol#configuring-mcp-servers)
for instructions on managing MCP configuration.

In `~/.cursor/mcp.json`:

```json
{
  "mcpServers": {
    "strands": {
      "command": "uvx",
      "args": ["strands-agents-mcp-server"]
    }
  }
}
```

## Server development

```bash
git clone https://github.com/strands-agents/mcp-server.git
cd mcp-server
python3 -m venv venv
source venv/bin/activate
pip3 install -e .

npx @modelcontextprotocol/inspector python -m strands_mcp_server
```

## Security

See [CONTRIBUTING](CONTRIBUTING.md#security-issue-notifications) for more information.

## License

This project is licensed under the Apache-2.0 License.
