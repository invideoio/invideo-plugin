# invideo

Plugin that connects agents to [invideo](https://invideo.io) through invideo's remote [Model Context Protocol](https://modelcontextprotocol.io/) server.

Make videos with invideo: generate media, edit timelines, and export.

## Install

### Cursor

1. Open **Cursor Settings → Plugins**.
2. Search for **invideo**.
3. Click **Install**, then sign in to invideo when prompted and choose the workspace the agent works in.

### Any other MCP client

```json
{
  "mcpServers": {
    "invideo": {
      "type": "http",
      "url": "https://mcp.invideo.io/mcp"
    }
  }
}
```

Auth is OAuth 2.1 with PKCE and Dynamic Client Registration. Your client asks you to sign in to invideo when it connects; there is no API key or client ID to configure. Each connection works in the one workspace chosen at sign-in.

## Notes

- Every tool takes a project URL as `url`, and every result gives the URLs to use next. Open any of them in a browser to see what the agent made.
- While an agent works on a timeline, people with the project open see it in the editor, with its cursor.
- Agents can call `get_help` for guidance and `report_bug` or `request_feature` to reach the invideo team.

## License

MIT
