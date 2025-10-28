# Runbook – {{título}}

**Última atualização:** {{data}}  
**Responsável:** {{nome}}

## Objetivo
Procedimento para {{ex: restaurar backup, girar segredos, lidar com incidentes}}.

## Pré-requisitos
- Acesso: {{ex: produção read-only}}  
- Ferramentas: {{ex: kubectl, psql}}

## Passos
1. Conectar no ambiente {{ambiente}}  
2. Executar:
   ```bash
   {{comando}}
   ```
3. Validar:
   - Logs
   - Health checks

## Rollback
Como desfazer a ação, se necessário.

## Referências
- Documentação oficial
- ADR/RFC relacionada
