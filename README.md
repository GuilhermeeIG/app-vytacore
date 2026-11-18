<h1 align="center"> App VYTACore</h1>
<p align="center"><b>Plataforma de acompanhamento cliente ↔ especialista com gamificação no estilo Duolingo</b></p>

<p align="center">
<img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white" /> <img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=white" /> <img src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white" /> <img src="https://img.shields.io/badge/Express-000000?style=for-the-badge&logo=express&logoColor=white" /> <img src="https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white" /> <img src="https://img.shields.io/badge/Socket.io-010101?style=for-the-badge&logo=socketdotio&logoColor=white" /> <img src="https://img.shields.io/badge/Tailwind%20CSS-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white" />
</p>

>  O código-fonte deste projeto é **privado**. Este repositório é uma vitrine com a visão geral, a arquitetura e a stack. Quer saber mais? Fale comigo pelo [LinkedIn](https://www.linkedin.com/in/luiz-guilherme-dos-santos-820a792a4/).

##  O que é

Um web app (PWA) que conecta clientes a especialistas e mantém o cliente engajado com uma camada de retenção gamificada: trilha diária, sequência (streak), XP, ligas semanais, missões, duplas e loja de moedas.

##  Destaques

-  **Chat em tempo real** entre cliente e especialista com Socket.io
-  **Gamificação completa**: ledger de XP idempotente, ligas, missões, conquistas e ofensiva
-  **Pagamentos recorrentes** com Asaas, webhooks idempotentes e controle de pendências
-  **Notificações push** (Web Push/VAPID) e e-mails transacionais com Resend
-  **Segurança e LGPD**: JWT em cookie httpOnly, validação com Zod, Helmet, rate limit, moderação de comunidade, exclusão de conta e criptografia em repouso
-  **Área do profissional** com carteira, faturamento, revisões e gestão de alunos
-  **Testes e2e** cobrindo gamificação, multi-especialista, concorrência e sockets

##  Arquitetura

```
 PWA (React + Vite + Tailwind)  ──HTTPS / WebSocket──▶  API (Node.js + Express + TypeScript)
                                                            ├─ MongoDB (Mongoose)
                                                            ├─ Asaas (pagamentos)
                                                            ├─ Resend (e-mail)
                                                            ├─ Web Push
                                                            └─ Sentry (erros)
```

##  Em números

| | |
|---|---|
| Endpoints REST | 70+ |
| Telas (cliente + profissional) | 76 |
| Componentes reutilizáveis | 64 |
| Linhas de código | ~35 mil |

##  Stack

- **Frontend:** React · TypeScript · Vite · Tailwind CSS · Radix/shadcn · TanStack Query · PWA
- **Backend:** Node.js · Express · TypeScript · Mongoose · Socket.io · Zod · JWT
- **Infra:** Render · MongoDB Atlas · Cloudflare · Sentry
