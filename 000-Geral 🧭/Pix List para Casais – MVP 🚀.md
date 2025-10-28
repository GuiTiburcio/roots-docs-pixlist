---
# YAML Frontmatter / Propriedades da Nota
tipo_nota: PRD
status: MVP_Em_Progresso  # Ex: Ideia, Discovery, MVP_Em_Progresso, Lançado, Arquivado
prioridade: Alta
crono_mvp: 2-3_semanas
prd_versao: 1.0
data_criacao: "2025-10-26"
time: [Eu, Parceiro] # Se houver parceiros
produto: Pix_List_Casais
---
## 📍 Problema (Dor do Usuário)

Casais precisam de lista prática e **"pixável"**, com temas, sem burocracia. A criação de listas de presentes tradicionais é lenta e a contribuição é limitada ou burocrática.

## 🎯 Objetivo do MVP

Criar e compartilhar a lista em **< 5 minutos** e receber contribuições via **Pix** de forma simples e imediata.

## 👤 Usuário-Alvo

* [[Noivos/as]]
* [[Madrinhas/Padrinhos]]
* Convidados que buscam praticidade.

## 📈 KPIs (Key Performance Indicators)

| Métrica | Objetivo | Descrição |
| :--- | :--- | :--- |
| **Conversão Visitante → Lista** | $\geq 15\%$ | Porcentagem de visitantes da página inicial que criam uma lista. |
| **1º Pix por Lista** | $\geq 30\%$ | Porcentagem de listas criadas que recebem pelo menos 1 contribuição Pix. |
| **TMA (Tempo Médio de Ação)** | $\leq 5$ minutos | Tempo total desde o início do onboarding até a lista estar **online** e **pronta para receber Pix**. |

## 📦 Escopo do MVP

### ✅ Dentro (In-Scope)

* **Passos de Onboarding Simplificados** (foco no TMA)
* **Geração IA** (Sugestão de temas/itens de lista baseada em prompts curtos)
* **Página Pública da Lista** (Link compartilhável e otimizado para mobile)
* **Pix Dinâmico / QR Code** (Geração de QR Code e Código Copia-e-Cola para a contribuição)
* **Webhook / Notificação de Pix** (Alerta imediato do recebimento)
* **Captura de Leads** (Email/Whatsapp dos criadores de listas)

### ❌ Fora (Out-of-Scope)

* **Marketplace** (Venda de produtos físicos ou integração com e-commerce)
* **Cupons Complexos** (Foco no Pix, sem a complexidade de códigos de desconto)
* **Multimoeda** (Apenas Pix/Real BRL)

## ⚠️ Riscos

* **Integração Pix/PSP:** Garantir a estabilidade e a legalidade da integração com o Provedor de Serviços de Pagamento (PSP).
* **Abandono na Etapa de Pagamento:** O processo de Pix (criação da chave/ID) pode ser um ponto de atrito.

## ⏳ Cronograma (MVP)

* **Estimativa:** 2 – 3 semanas.
* **[Link para o Quadro Kanban](link_interno_para_quadro_kanban)** (se usar o plugin Kanban)

### Tarefas Chave (com checklist Markdown)

- [ ] Definir o fluxo exato de Onboarding.
- [ ] Integrar com o PSP para geração de Pix.
- [ ] Desenvolver a página pública (design minimalista).
- [ ] Criar o prompt base para a Geração IA.

---

## 🔗 Próximos Passos/Discussões

* [[Brainstorm - Temas e Prompts IA]]
* [[Reunião - Integração Pix e PSPs]]