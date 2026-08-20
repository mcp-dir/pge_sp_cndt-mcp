---
name: pge_sp_cndt-mcp
description: Skill da REST API do Procuradoria Geral do Estado SP: Certidão Negativa de Débitos Tributários na MCP.AI: 1 endpoint em /api/pge_sp_cndt. Procuradoria Geral do Estado SP: Certidão Negativa de Débitos Tributários, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago. Autentique com workspace API key (sk_live) gerada em app.mcp.ai/settings/api-keys. Use quando o usuário pedir algo coberto pelos endpoints.
---

# Procuradoria Geral do Estado SP: Certidão Negativa de Débitos Tributários — REST API skill

Você tem acesso à **Procuradoria Geral do Estado SP: Certidão Negativa de Débitos Tributários** REST API na MCP.AI.

> Procuradoria Geral do Estado SP: Certidão Negativa de Débitos Tributários, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago.

## Base URL

```
https://api.mcp.ai/api/pge_sp_cndt
```

Todo endpoint é um **POST** na Base URL + o path abaixo. Os parâmetros vão no corpo JSON.

## Autenticação

Inclua em toda request:

```
Authorization: Bearer sk_live_...
Content-Type: application/json
```

> Gere sua chave em **https://app.mcp.ai/settings/api-keys** (workspace API key `sk_live_…`, não expira, revogável). Uma única chave serve pra todos os seus MCPs.

## Formato de resposta

```json
{ "ok": true, "tool": "<tool_id>", "result": <payload> }
```

## Exemplo cURL

```bash
curl -X POST https://api.mcp.ai/api/pge_sp_cndt/consultar \
  -H "Authorization: Bearer sk_live_..." \
  -H "Content-Type: application/json" \
  -d '{}'
```

## Reportar problemas

Se um endpoint retornar erro, vazio ou dado inesperado, reporte (não desista calado): **POST /api/pge_sp_cndt/report** com `{ "message": "...", "context"?: "...", "conversation"?: [...] }`. Isso notifica o time da MCP.AI.

## Endpoints (1)

#### `pge_sp_cndt_consultar`

Procuradoria Geral do Estado SP: Certidão Negativa de Débitos Tributários, consulta em fonte oficial. _(POST /api/pge_sp_cndt/consultar)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `cnpj` | string | Não | Parâmetro de consulta "cnpj". |
| `cpf` | string | Não | Parâmetro de consulta "cpf". |
| `login_cpf` | string | Não | Parâmetro de consulta "login_cpf". |
| `login_senha` | string | Não | Parâmetro de consulta "login_senha". |
| `pkcs12_cert` | string | Não | Parâmetro de consulta "pkcs12_cert". |
| `pkcs12_pass` | string | Não | Parâmetro de consulta "pkcs12_pass". |

---

Este MCP também funciona via **conexão MCP** (Claude / Cursor) em `https://api.mcp.ai/p_pge_sp_cndt` — veja o [README](../../README.md). A skill acima é pra consumir a **REST API** direto (agente próprio / código).
