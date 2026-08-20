---
name: incra_sigef_requerimentos-mcp
description: Skill da REST API do INCRA SIGEF: Requerimentos na MCP.AI: 1 endpoint em /api/incra_sigef_requerimentos. INCRA SIGEF: Requerimentos, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago. Autentique com workspace API key (sk_live) gerada em app.mcp.ai/settings/api-keys. Use quando o usuário pedir algo coberto pelos endpoints.
---

# INCRA SIGEF: Requerimentos — REST API skill

Você tem acesso à **INCRA SIGEF: Requerimentos** REST API na MCP.AI.

> INCRA SIGEF: Requerimentos, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago.

## Base URL

```
https://api.mcp.ai/api/incra_sigef_requerimentos
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
curl -X POST https://api.mcp.ai/api/incra_sigef_requerimentos/consultar \
  -H "Authorization: Bearer sk_live_..." \
  -H "Content-Type: application/json" \
  -d '{"login_cpf":"...","login_senha":"..."}'
```

## Reportar problemas

Se um endpoint retornar erro, vazio ou dado inesperado, reporte (não desista calado): **POST /api/incra_sigef_requerimentos/report** com `{ "message": "...", "context"?: "...", "conversation"?: [...] }`. Isso notifica o time da MCP.AI.

## Endpoints (1)

#### `incra_sigef_requerimentos_consultar`

INCRA SIGEF: Requerimentos, consulta em fonte oficial. _(POST /api/incra_sigef_requerimentos/consultar)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `cpf` | string | Não | Parâmetro de consulta "cpf". |
| `cnpj` | string | Não | Parâmetro de consulta "cnpj". |
| `codigo_imovel` | string | Não | Parâmetro de consulta "codigo_imovel". |
| `protocolo` | string | Não | Parâmetro de consulta "protocolo". |
| `pagina` | string | Não | Parâmetro de consulta "pagina". |
| `login_cpf` | string | Sim | Parâmetro de consulta "login_cpf". |
| `login_senha` | string | Sim | Parâmetro de consulta "login_senha". |
| `pkcs12_cert` | string | Não | Parâmetro de consulta "pkcs12_cert". |
| `pkcs12_pass` | string | Não | Parâmetro de consulta "pkcs12_pass". |

---

Este MCP também funciona via **conexão MCP** (Claude / Cursor) em `https://api.mcp.ai/p_incra_sigef_requerimentos` — veja o [README](../../README.md). A skill acima é pra consumir a **REST API** direto (agente próprio / código).
