# Instalação rápida

Procuradoria Geral do Estado SP: Certidão Negativa de Débitos Tributários é um servidor MCP remoto hospedado em `https://api.mcp.ai/p_pge_sp_cndt`. Você não baixa nem roda nada localmente — só aponta seu cliente pra essa URL.

A auth acontece em runtime: clientes com **OAuth 2.1** (Claude Desktop, Cursor, VS Code recentes) abrem o browser na 1ª chamada (magic-link). Clientes sem OAuth recebem a tool `authenticate` — abra `https://app.mcp.ai/agent-auth`, faça login, copie o JWT e cole no chat.

---

## Claude (Web e Desktop)

[➕ Abrir no Claude e conectar](https://claude.ai/new?modal=add-custom-connector#settings/customize-connectors)

Manual: [claude.ai/customize/connectors](https://claude.ai/customize/connectors?surface=cowork) → **+** → **Adicionar conector personalizado** → `Procuradoria Geral do Estado SP: Certidão Negativa de Débitos Tributários` / `https://api.mcp.ai/p_pge_sp_cndt`.

Config file (legado): `~/Library/Application Support/Claude/claude_desktop_config.json` (macOS) ou `%APPDATA%\Claude\claude_desktop_config.json` (Windows):

```json
{ "mcpServers": { "pge_sp_cndt": { "type": "http", "url": "https://api.mcp.ai/p_pge_sp_cndt" } } }
```

## Cursor

[➕ Instalar no Cursor](cursor://anysphere.cursor-deeplink/mcp/install?name=pge_sp_cndt&config=eyJ1cmwiOiJodHRwczovL2FwaS5tY3AuYWkvcF9wZ2Vfc3BfY25kdCJ9)

`.cursor/mcp.json`:
```json
{ "mcpServers": { "pge_sp_cndt": { "url": "https://api.mcp.ai/p_pge_sp_cndt" } } }
```

## VS Code (Copilot Chat)

[➕ Instalar no VS Code](vscode:mcp/install?name=pge_sp_cndt&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fapi.mcp.ai%2Fp_pge_sp_cndt%22%7D)

`.vscode/mcp.json`:
```json
{ "servers": { "pge_sp_cndt": { "type": "http", "url": "https://api.mcp.ai/p_pge_sp_cndt" } } }
```

## Outros clientes MCP

Qualquer cliente com **MCP over HTTP**. URL fixa:

```
https://api.mcp.ai/p_pge_sp_cndt
```

Dúvidas? [pge_sp_cndt@mcp.ai](mailto:pge_sp_cndt@mcp.ai)
