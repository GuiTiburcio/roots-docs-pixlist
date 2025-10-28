# Rotação de Segredos – {{sistema}}

## Escopo
- Segredos: {{API keys, JWT secrets, DB passwords}}
- Ambientes: {{dev, stage, prod}}

## Procedimento
1. Gerar segredo novo de forma segura
2. Atualizar em {{ex: Vault/Secret Manager}}
3. Atualizar variáveis no CI/CD
4. Programar deploy sem downtime
5. Revogar segredo antigo

## Validação
- Testes de autenticação
- Logs sem erros
