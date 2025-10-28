# API Spec – {{Nome da API}}

**Versão:** v{{n}}  
**Owner:** {{nome}}  
**Última atualização:** {{data}}

## Descrição
{{Resumo do propósito da API}}

## Endpoint
`{{METHOD}} /api/{{rota}}`

### Request
```json
{
  "{{campo}}": "{{valor}}"
}
```

### Response (200)
```json
{
  "success": true,
  "data": { }
}
```

### Erros
| Código | Mensagem | Descrição |
|--------|----------|-----------|
| 400 | Invalid Input | Campos obrigatórios ausentes |
| 401 | Unauthorized | Falha na autenticação |
| 429 | Too Many Requests | Rate limiting |

## Segurança
- Autenticação: {{ex: JWT, OAuth2, sessão}}  
- Rate limiting: {{ex: 60 req/min por IP}}  
- PII: {{ex: campos anonimizados}}

## Contratos relacionados
- DB: tabela `{{tabela}}`
- Serviço: `{{service}}`
- Schema: `{{link}}`
