# Instalação detalhada

INCRA SIGEF: Requerimentos é um servidor MCP remoto. Aponte seu cliente pra `https://api.mcp.ai/p_incra_sigef_requerimentos`. Snippets rápidos: [INSTALL.md](../INSTALL.md).

| Cliente | URL | Auth |
|---|---|---|
| Claude Desktop | `https://api.mcp.ai/p_incra_sigef_requerimentos` | OAuth 2.1 ou agent-auth |
| Cursor | `https://api.mcp.ai/p_incra_sigef_requerimentos` | OAuth 2.1 ou agent-auth |
| VS Code (Copilot) | `https://api.mcp.ai/p_incra_sigef_requerimentos` | OAuth 2.1 ou agent-auth |

A config JSON é a mesma em todos: só a URL, sem headers.

## Desinstalar

Remova o bloco `mcpServers.incra_sigef_requerimentos` (ou `servers.incra_sigef_requerimentos` no VS Code) do config do cliente e reinicie.
