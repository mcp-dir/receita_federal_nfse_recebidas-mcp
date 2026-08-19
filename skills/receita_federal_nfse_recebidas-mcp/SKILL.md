---
name: receita_federal_nfse_recebidas-mcp
description: Skill da REST API do Receita Federal NFS-e: Notas Recebidas na MCP.AI: 1 endpoint em /api/receita_federal_nfse_recebidas. Receita Federal NFS-e: Notas Recebidas, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago. Autentique com workspace API key (sk_live) gerada em app.mcp.ai/settings/api-keys. Use quando o usuário pedir algo coberto pelos endpoints.
---

# Receita Federal NFS-e: Notas Recebidas — REST API skill

Você tem acesso à **Receita Federal NFS-e: Notas Recebidas** REST API na MCP.AI.

> Receita Federal NFS-e: Notas Recebidas, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago.

## Base URL

```
https://api.mcp.ai/api/receita_federal_nfse_recebidas
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
curl -X POST https://api.mcp.ai/api/receita_federal_nfse_recebidas/consultar \
  -H "Authorization: Bearer sk_live_..." \
  -H "Content-Type: application/json" \
  -d '{}'
```

## Reportar problemas

Se um endpoint retornar erro, vazio ou dado inesperado, reporte (não desista calado): **POST /api/receita_federal_nfse_recebidas/report** com `{ "message": "...", "context"?: "...", "conversation"?: [...] }`. Isso notifica o time da MCP.AI.

## Endpoints (1)

#### `receita_federal_nfse_recebidas_consultar`

Receita Federal NFS-e: Notas Recebidas, consulta em fonte oficial. _(POST /api/receita_federal_nfse_recebidas/consultar)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `pkcs12_cert` | string | Não | Parâmetro de consulta "pkcs12_cert". |
| `pkcs12_pass` | string | Não | Parâmetro de consulta "pkcs12_pass". |
| `login_cpf` | string | Não | Parâmetro de consulta "login_cpf". |
| `login_cnpj` | string | Não | Parâmetro de consulta "login_cnpj". |
| `login_senha` | string | Não | Parâmetro de consulta "login_senha". |
| `data_inicial` | string | Não | Parâmetro de consulta "data_inicial". |
| `data_final` | string | Não | Parâmetro de consulta "data_final". |
| `pagina` | string | Não | Parâmetro de consulta "pagina". |

---

Este MCP também funciona via **conexão MCP** (Claude / Cursor) em `https://api.mcp.ai/p_receita_federal_nfse_recebidas` — veja o [README](../../README.md). A skill acima é pra consumir a **REST API** direto (agente próprio / código).
