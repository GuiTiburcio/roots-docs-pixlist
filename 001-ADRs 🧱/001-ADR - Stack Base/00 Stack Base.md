**Status:** Accepted  
**Data:** 2025-10-26  

## Contexto
Definir a base tecnológica do projeto Roots (PixList).

## Decisão
Utilizar Next.js + NestJS + PostgreSQL como stack principal.

## Consequências
- Adoção de TypeScript full-stack.
- Infra simplificada para deploy.](<Data: %3CYYYY-MM-DD%3E>)

## Contexto
Precisamos de um stack que suporte rápido desenvolvimento, SSR/SSG para SEO (blog), integração com APIs, e deploy fácil.

## Decisão
Escolhemos:
- Frontend/App: Next.js 14+ (App Router) em TypeScript
- UI: Tailwind CSS + shadcn/ui
- DB: PostgreSQL (Supabase / Railway) com Prisma
- Auth: NextAuth (magic link)
- Pagamentos: PSP que suporte Pix Dinâmico; webhooks para confirmação
- Infra: Vercel, S3-compatible para assets
- Observabilidade: Sentry + Logtail
- Jobs: Upstash/Cloudflare Queues
- Validação: Zod

## Alternativas consideradas
- Usar Firebase (rejeitado por lock-in e limite em queries complexas)
- Usar Rails (boa, mas menos alinhado ao ecossistema JS/TS)
- Auth0 (alto custo e overkill neste estágio)

## Impacto
- Produtividade alta para frontend e SEO.
- Fácil integração com mobile futuro (React Native).
