# Weather MCP Server

[Tutorial link](https://modelcontextprotocol.io/quickstart/server#node)

## Run project

1. Clone the server repository

```bash
git clone <repository-url>
cd weather-mcp-server
```

2. Build MCP server

```bash
npm run build
```

3. Add MCP server to claude_desktop_config.json file

```bash
{
  "mcpServers": {
    "weather": {
      "command": "node",
      "args": ["/ABSOLUTE/PATH/TO/PARENT/FOLDER/weather/build/index.js"]
    }
  }
}
```

4. Run the MCP server

```bash
node /ABSOLUTE/PATH/TO/PARENT/FOLDER/weather/build/index.js
```

5. Restart Claude Desktop. Ask Claude questions like "What’s the weather in Sacramento?" or "What are the active weather alerts in Texas?" to test the MCP server.