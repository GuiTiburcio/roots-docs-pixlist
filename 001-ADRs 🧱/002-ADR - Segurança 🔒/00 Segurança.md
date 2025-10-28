**Status:** Accepted  
**Data:** 2025-10-26  

## Contexto
Definir padrões mínimos de segurança.

## Decisão
Aplicar autenticação via NextAuth, rotinas de refresh token e logs seguros.

## Consequências
- Sessões mais confiáveis.
- Proteção contra acessos indevidos.](<Data: %3CYYYY-MM-DD%3E>)

## Contexto
A aplicação lida com transações via Pix e dados pessoais. Requer práticas robustas.

## Decisão
- CSP estrita, HSTS, X-Frame-Options, X-Content-Type-Options.
- Rate limiting em endpoints críticos.
- Webhooks assinados HMAC + idempotência.
- Logs imutáveis e observabilidade (Sentry).
- TLS 1.3 obrigatório.
- No storage de dados bancários.

## Alternativas
- Delegar tudo ao PSP (viável), mas manter verificação e logs locais.

## Impacto
Maior segurança operacional e conformidade com melhores práticas.
