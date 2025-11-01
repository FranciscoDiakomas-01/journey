# ⚙️ OmniPOS AI — Documento Técnico Interno

> Estrutura técnica, arquitetura e detalhes de desenvolvimento da plataforma.

---

## 🧠 Serviços e Responsabilidades

| Serviço                  | Função                           | Tecnologias         |
| ------------------------ | -------------------------------- | ------------------- |
| **Auth Service**         | JWT, OAuth, controle de sessão   | NestJS + Passport   |
| **AI Service**           | Recomendações e Chatbot          | LangChain + OpenAI  |
| **Catalog Service**      | CRUD de produtos e sincronização | Prisma + PostgreSQL |
| **POS Service**          | Registro de vendas e relatórios  | Redis + PostgreSQL  |
| **Notification Service** | WhatsApp, E-mail, Push           | Twilio, Nodemailer  |
| **Analytics Service**    | Insights automáticos             | Metabase + OpenAI   |
| **Search Service**       | Busca de produtos e pedidos      | Meilisearch         |

---

## 🔐 Autenticação

- JWT para API REST
- OAuth (Google, Facebook, WhatsApp)
- Suporte a login por link mágico (Magic Link via e-mail)

---

## 🧩 APIs Externas Recomendadas

| Categoria     | API                                     | Uso                         |
| ------------- | --------------------------------------- | --------------------------- |
| 💬 WhatsApp   | Twilio API / WhatsApp Cloud API         | Mensagens automáticas e bot |
| 💳 Pagamentos | Stripe / Multicaixa / PayPay            | Checkout online             |
| 📦 Entregas   | Google Maps API / App de delivery local | Rotas e rastreio            |
| 🧠 IA         | OpenAI / HuggingFace / LangChain        | Recomendação e NLP          |
| 🔍 Busca      | Meilisearch                             | Busca de catálogo           |

---

## 🧰 DevOps Essentials

- **Docker Compose** para orquestração
- **Railway ou Render** para backend
- **Vercel** para frontend
- **Cloudflare R2 / S3** para armazenamento
- **CI/CD** via GitHub Actions

---

## 📦 Cache e Performance

- **Redis** para cache de IA e sessões
- **Keyv** para cache de prompts LangChain
- **Rate limiting** para APIs sensíveis

---

## 🧠 Melhoria Contínua

- Log centralizado com **Winston + Loki + Grafana**
- Testes automatizados (Jest + Supertest)
- Monitoramento de uso com PostHog

---

## 🧭 Roadmap Técnico

1️⃣ MVP — POS + Catálogo Online  
2️⃣ IA Chatbot + WhatsApp Integration  
3️⃣ Dashboard IA + Analytics  
4️⃣ App Mobile com React Native  
5️⃣ Automação de Estoque e Marketing

---

## 👨‍💻 Contato Interno

Dev Lead: **Francisco Diakomas**  
E-mail: `franciscodiakomas@journey.dev`
