# Server-Sent Events (SSE) Connection

⚠️ **Deprecated** - SSE as a standalone transport has been deprecated in favor of **Streamable HTTP**.

## What Happened to SSE?

In protocol revision **2025-03-26**, **Streamable HTTP** replaced the older HTTP+SSE transport defined in revision 2024-11-05. See the [official MCP specification](https://modelcontextprotocol.io/specification/2025-03-26/basic/transports#streamable-http).

## Current MCP Transport Options

The MCP specification now defines only **two standard transport mechanisms**:

1. **[stdio](./stdio.md)** - Communication over standard in and standard out
1. **[Streamable HTTP](./streamable_http.md)** - HTTP-based communication with optional SSE support

## What This Means

- **SSE functionality is still available** - but as part of Streamable HTTP, not as a standalone transport
- **Streamable HTTP can use SSE** - for server-to-client streaming when needed
- **Legacy HTTP+SSE servers remain compatible** - Clients and servers can still support the older transport using the spec's [backwards-compatibility guidance](https://modelcontextprotocol.io/specification/2025-03-26/basic/transports#backwards-compatibility). Prefer Streamable HTTP for new integrations

## Migration Path

If you were planning to use SSE, consider:

- **[Streamable HTTP](./streamable_http.md)** - The modern replacement that includes SSE capabilities
- **[Local Process (stdio)](./stdio.md)** - For local server connections
- **[WebSocket](./websocket.md)** - For full-duplex real-time communication (custom transport)

## Next Steps

- **[Streamable HTTP](./streamable_http.md)** - The modern HTTP transport with SSE capabilities
- **[Local Process (stdio)](./stdio.md)** - Local server connections with many examples
- **[Example MCP Servers](../servers/index.md)** - Available server examples
