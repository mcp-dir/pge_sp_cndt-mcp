# Instalação detalhada

Procuradoria Geral do Estado SP: Certidão Negativa de Débitos Tributários é um servidor MCP remoto. Aponte seu cliente pra `https://api.mcp.ai/p_pge_sp_cndt`. Snippets rápidos: [INSTALL.md](../INSTALL.md).

| Cliente | URL | Auth |
|---|---|---|
| Claude Desktop | `https://api.mcp.ai/p_pge_sp_cndt` | OAuth 2.1 ou agent-auth |
| Cursor | `https://api.mcp.ai/p_pge_sp_cndt` | OAuth 2.1 ou agent-auth |
| VS Code (Copilot) | `https://api.mcp.ai/p_pge_sp_cndt` | OAuth 2.1 ou agent-auth |

A config JSON é a mesma em todos: só a URL, sem headers.

## Desinstalar

Remova o bloco `mcpServers.pge_sp_cndt` (ou `servers.pge_sp_cndt` no VS Code) do config do cliente e reinicie.
