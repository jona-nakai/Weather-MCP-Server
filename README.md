# Weather MCP Server

An MCP server that utilizes https://api.weather.gov api to gather weather alerts and forecast through the Claude Desktop applicaiton.

[Tutorial link](https://modelcontextprotocol.io/quickstart/server#node)

## Run project

1. Clone the server repository

```bash
git clone <repository-url>
cd weather-mcp-server
```

2. Install dependencies

```bash
npm install @modelcontextprotocol/sdk zod@3
npm install -D @types/node typescript
```

3. Build MCP server

```bash
npm run build
```

4. Add MCP server to claude_desktop_config.json file

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

5. Run the MCP server

```bash
node /ABSOLUTE/PATH/TO/PARENT/FOLDER/weather/build/index.js
```

6. Restart Claude Desktop. Ask Claude questions like "What’s the weather in Sacramento?" or "What are the active weather alerts in Texas?" to test the MCP server.