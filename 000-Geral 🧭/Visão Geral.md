# 🌱 Visão Geral

O **Roots (PixList)** é uma plataforma que permite a criação de listas de presentes de casamento baseadas em transações Pix.

## 🎯 Objetivo
Oferecer uma solução moderna, simples e segura para casais receberem presentes de forma digital.

## 🚀 Principais módulos
- Onboarding dos noivos
- Criação da lista de presentes
- Checkout via Pix
- Dashboard de controle


Uma plataforma que permite casais criarem uma “Pix List” temática para chá de panela/casa nova: o casal escolhe um tema (vintage, clássico, moderno, old-futurista etc.), gera uma lista inteligente (essenciais/recomendados/nice-to-have), publica uma página com QR Pix por item/valor e acompanha pagamentos. O produto também serve como motor de geração de leads (blog/SEO, página pública, captura de contatos com consentimento LGPD).

# 🌿 Roots – PixList Docs
> “Crescendo raízes fortes para um produto sólido.”

## 🧭 Geral
- [[Visão-Geral]]
- [[Arquitetura]]
- [[Stack]]

## 📅 Roadmap
- [[📅 003-Roadmap/Sprints/Sprint-01]]
- [[Epic-Checkout]]

## 💬 RFCs
- [[RFC-001-API-Checkout]]

## 🧱 ADRs
- [[001-Stack-Base]]
- [[002-Segurança]]
- [[003-LGPD]]

## ⚙️ Runbooks
- [[Incident-Guide]]
- [[Backup-Restore]]

## Decisões iniciais (Architecture Decision Records – ADR)

Crie 1 ADR por decisão relevante no diretório `docs/adr/`.

### **ADR-001 – Stack base**

- **Frontend/App**: Next.js 14+ (App Router) em TypeScript
    
- **UI**: Tailwind + shadcn/ui
    
- **DB**: PostgreSQL (Supabase/Railway) via Prisma ORM
    
- **Auth**: NextAuth (email magic link; OAuth opcional)
    
- **Pagamentos**: PSP com Pix Dinâmico e Webhooks
    
- **Infra**: Vercel (app + funções serverless); Storage S3-compatible para assets (opcional)
    
- **Observabilidade**: Sentry + Logtail/Better Stack
    
- **Filas/Jobs**: Upstash/Cloudflare Queues (agradecimentos e processamento de webhooks)
    
- **Validação**: Zod end-to-end
    

### **ADR-002 – Segurança**

- CSP estrita, HSTS, headers de segurança, rate limit, idempotência em cobranças, assinatura HMAC de webhook, logs imutáveis.
    

### **ADR-003 – LGPD**

- Bases legais: execução de contrato (serviço), consentimento (marketing), interesse legítimo (analytics first‑party limitado).
    
- Minimização: coletar apenas dados necessários (nome e contato do pagador – opcionais).
    
- DSR: endpoint para exportar/apagar dados; retenção 24 meses + anonimização.
    

> **Como documentar**: cada ADR tem contexto, decisão, alternativas, trade-offs e impacto.

## 4) Sugestão de ferramentas e por onde começar (ordem prática)

1. **Design/Prototipagem:** Figma (UI kit + layouts) — opcional Stitch para tokens visuais.
    
2. **Notas / ADRs / Roadmap:** Obsidian (ou Notion) — criar vault `pixlist`.
    
3. **Repositório:** GitHub monorepo (pnpm).
    
4. **IDE:** VSCode (extensões instaladas).
    
5. **Scaffold:** create-next-app + TypeScript → configurar Tailwind → Prisma → NextAuth.
    
6. **Implementar landing + lead form** (primeira iteração).
    
7. **Criar DB e Prisma migrations** com seed data (templates).
    
8. **Criar auth + dashboard minimal**.
    
9. **Stub de pagamentos (create-pix)** e webhook handler.
    
10. **Testes + lint + CI** → deploy preview em Vercel.
    
11. **Observability + backup**.
    

## 5) Integração IA para debugging

- Use **GitHub Copilot** para produtividade de código.
    
- Use **ChatGPT / Cursor** para revisar PRs e explicar mudanças.
    
- Automatize PR checks que rodam testes + lint + execução de “explain” (usar comentários gerados pela IA como base).
    
- Para correção automática, combine Copilot + Codeium + revisão humana — nunca deploy automático sem revisão em prod.