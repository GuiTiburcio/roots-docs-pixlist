**_Specifications_** — ou seja, **especificações técnicas** do produto, principalmente relacionadas a **APIs, contratos e integrações**.

`specs/` é o lugar onde você documenta **como o sistema se comunica internamente e externamente** —  
o “como funciona por baixo do capô”.

---

### 🧩 **O que normalmente entra em `specs/`:**

|Tipo de arquivo|Função|Exemplo prático|
|---|---|---|
|**API Spec**|Define endpoints, métodos HTTP, payloads, respostas, erros, autenticação.|`/api/payments/create-pix` → `POST` com JSON de entrada e saída.|
|**DB Schema Spec**|Descreve tabelas, colunas e relacionamentos.|Tabela `transactions` → `id`, `user_id`, `amount`, `status`.|
|**Contract Spec**|Define contratos entre serviços ou integrações externas.|Integração com **Pix**, **Supabase**, ou **gateway de email**.|
|**Validation Rules**|Regras de negócio e validação.|“O valor mínimo para presente é R$ 10,00.”|
|**Event Spec**|Define eventos internos (ex: Webhooks, RabbitMQ, Kafka).|“Evento `payment.completed` é disparado quando um Pix é confirmado.”|