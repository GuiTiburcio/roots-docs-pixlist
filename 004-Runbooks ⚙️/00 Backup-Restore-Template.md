# Backup & Restore – {{banco/sistema}}

## Política de backup
- Frequência: {{ex: diário às 02:00 UTC}}
- Retenção: {{ex: 30 dias}}

## Restaurar
1. Localizar snapshot {{data/hora}}
2. Executar restore:
   ```bash
   {{comando de restore}}
   ```
3. Validar consistência (checksums, contagens)

## Teste periódico
- Simular restore 1x por mês
