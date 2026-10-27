<div align="center">
  <h1>🧗 Aresta Climb</h1>
  <p><strong>Croquis interativos, guias de escalada em rocha e base de dados 100% livre e offline-first.</strong></p>

  <p>
    <a href="https://arestaclimb.com"><img src="https://img.shields.io/badge/Site-arestaclimb.com-16a34a?style=flat-square&logo=googlechrome&logoColor=white" alt="Site Oficial" /></a>
    <a href="https://arestaclimb.com/editor"><img src="https://img.shields.io/badge/Editor_Desktop-arestaclimb.com%2Feditor-0284c7?style=flat-square&logo=desktop&logoColor=white" alt="Aresta Editor" /></a>
    <a href="https://arestaclimb.com/app"><img src="https://img.shields.io/badge/App-Android_%26_iOS-2563eb?style=flat-square&logo=flutter&logoColor=white" alt="Baixar App" /></a>
    <a href="https://chat.whatsapp.com/JmxWeLSmGTT66AREtrKyjA"><img src="https://img.shields.io/badge/Comunidade-WhatsApp-25D366?style=flat-square&logo=whatsapp&logoColor=white" alt="Comunidade no WhatsApp" /></a>
    <a href="https://instagram.com/arestaclimb"><img src="https://img.shields.io/badge/Instagram-@arestaclimb-E4405F?style=flat-square&logo=instagram&logoColor=white" alt="Instagram @arestaclimb" /></a>
    <a href="https://sentry.io/?utm_source=github&utm_medium=referral"><img src="https://img.shields.io/badge/Monitorado_com-Sentry-362D59?style=flat-square&logo=sentry&logoColor=white" alt="Monitorado com Sentry" /></a>
  </p>
</div>

---

## 🏔️ Sobre o Projeto

O **Aresta Climb** é um ecossistema de código aberto criado por escaladores para preservar a história da escalada, estruturar croquis interativos e garantir que a informação chegue ao pé da via **100% offline**, respeitando integralmente a autoria de conquistadores, desenhistas de croquis e associações locais.

Ao contrário de plataformas comerciais fechadas que trancam o trabalho coletivo da comunidade atrás de assinaturas, o Aresta separa claramente **código aberto (MPL 2.0)**, **metadados abertos (ODbL 1.0)** e **respeito ao trabalho** dos criadores originais.

---

## 📦 Repositórios do Ecossistema

| Repositório | Descrição | Tecnologias Principais | Licença |
| :--- | :--- | :--- | :--- |
| 📱 **[`aresta_app`](https://github.com/aresta-climb/aresta_app)** | Aplicativo mobile multiplataforma (Android & iOS) com navegação em árvore, croquis vetoriais interativos e Delta Sync atômico em background (`Isolate`). | Flutter, Dart, Protobuf (`binarypb`), SQLite | `MPL-2.0` |
| 🗄️ **[`aresta_db`](https://github.com/aresta-climb/aresta_db)** | Base de dados aberta de escalada, pipeline de compilação Protobuf/SQLite e o **[Aresta Editor](https://arestaclimb.com/editor)** (aplicativo desktop multiplataforma para criação visual de croquis e envio automatizado de Pull Requests). | Python, PySide6 (Qt), Protobuf, SQLite | `MPL-2.0` / `ODbL-1.0` |
| ⚡ **[`aresta_backend`](https://github.com/aresta-climb/aresta_backend)** | Infraestrutura serverless e de borda: proxy Git Smart HTTP (`git-proxy`), abertura assistida de PRs (`create-pr`), recebimento de feedbacks In-App (`app-feedback`), Delta Sync do catálogo e roteador de alertas. | Supabase Edge Functions (Deno/TS), PostgreSQL, Cloudflare Workers, D1, R2 | `MPL-2.0` |
| 🌐 **[`arestaclimb.com`](https://github.com/aresta-climb/arestaclimb.com)** | Portal institucional, hub de downloads mobile e do **[Aresta Editor](https://arestaclimb.com/editor)**, redirecionamento inteligente (`aresta.cc`) e documentação legal/técnica. | HTML5, CSS3, Vite, Vitest | `MPL-2.0` |

---

## 🤝 Comunidade & Canais Oficiais

O Aresta é construído junto com quem frequenta a rocha, equipa vias e mantém os setores vivos:

- 💬 **[Comunidade no WhatsApp](https://chat.whatsapp.com/JmxWeLSmGTT66AREtrKyjA):** Canal aberto para escaladores, conquistadores e colaboradores trocarem betas, sugerirem novos picos e acompanharem atualizações.
- 📸 **[Instagram (`@arestaclimb`)](https://instagram.com/arestaclimb):** Novidades de picos catalogados, lançamentos de recursos e histórias da comunidade.
- 🛠️ **Servidor no Discord:** Hub de engenharia, triagem de feedbacks da comunidade e alertas operacionais em tempo real.
- ✍️ **[Aresta Editor (`arestaclimb.com/editor`)](https://arestaclimb.com/editor):** Baixe o Editor Desktop (Windows, macOS e Linux) para desenhar e atualizar croquis visualmente sem precisar programar.

---

## 🛠️ Infraestrutura & Apoiadores

Mantemos uma arquitetura enxuta, resiliente e distribuída na borda, viabilizada por ferramentas de ponta e apoiadores do ecossistema Open Source:

### 💜 Apoio Oficial de Observabilidade — [Sentry](https://sentry.io/?utm_source=github&utm_medium=referral)

<p>
  <a href="https://sentry.io/?utm_source=github&utm_medium=referral">
    <img src="https://img.shields.io/badge/Sentry-Sponsored_Business_Plan-362D59?style=for-the-badge&logo=sentry&logoColor=white" alt="Sentry Sponsored Business Plan" />
  </a>
</p>

Agradecemos especialmente ao **[Sentry](https://sentry.io/?utm_source=github&utm_medium=referral)** pelo patrocínio ao Aresta Climb através do seu programa Open Source (**Sponsored Business Plan**). O Sentry monitora em tempo real nossas 4 frentes de código (**Mobile App em Flutter**, **Aresta Editor em Python/Qt**, **Supabase Edge Functions** e **Cloudflare Workers**), garantindo estabilidade em campo mesmo em condições extremas de conectividade.

### ⚙️ Stack de Infraestrutura

- **☁️ [Cloudflare](https://www.cloudflare.com/) (Workers, R2, D1, KV & Pages):** Distribuição global de pacotes `.binarypb` e imagens WebP com zero custo de *egress* (`serving.arestaclimb.com`), sincronização incremental SQLite em borda (`catalogo.arestaclimb.com`), App Links (`aresta.cc`) e fila resiliente de alertas (`alertas.arestaclimb.com`).
- **⚡ [Supabase](https://supabase.com/) (PostgreSQL, Auth & Edge Functions):** Autenticação de colaboradores do Editor Desktop, controle de revisões e proxy Git seguro para submissão de sugestões diretamente da comunidade.
- **🔥 [Firebase](https://firebase.google.com/) (Crashlytics, Analytics, Remote Config & App Check):** Telemetria nativa Android/iOS (`ANRs`/NDK) e proteção anti-abuso criptográfica (`App Check` via Play Integrity / App Attest).
- **📧 [Resend](https://resend.com/):** Entrega transacional de códigos de acesso (OTP) do Aresta Editor.
- **📊 [Umami Analytics](https://umami.is/) + [Vercel](https://vercel.com/) + [Google Cloud](https://cloud.google.com/):** Métricas web éticas, sem cookies invasivos e respeitando a privacidade do usuário (`analytics.arestaclimb.com`).
- **🔔 [GitHub Actions](https://github.com/features/actions) + [Discord](https://discord.com/) + [ntfy.sh](https://ntfy.sh/):** Pipeline de validação automatizada de croquis/licenças SPDX e operação ChatOps em tempo real.

---

## 🤝 Como Contribuir

Escaladores, conquistadores, mantenedores de picos e desenvolvedores são muito bem-vindos!
- Quer mapear um novo setor ou corrigir uma via? Baixe o **[Aresta Editor](https://arestaclimb.com/editor)** ou veja o **[Guia de Contribuição do `aresta_db`](https://github.com/aresta-climb/aresta_db/blob/main/CONTRIBUINDO.md)**.
- É autor de um croqui histórico? Veja como reivindicar autoria e autonomia de revisão em **[Guia para Autores](https://github.com/aresta-climb/aresta_db/blob/main/AUTORES.md)**.
- Quer contribuir com código? Confira nossos **[Princípios de Engenharia (`AGENTS.md`)](https://github.com/aresta-climb/aresta_app/blob/main/AGENTS.md)**.

---

## ⚖️ Licença

O código-fonte do ecossistema Aresta Climb é distribuído sob a licença **[Mozilla Public License 2.0 (MPL 2.0)](https://github.com/aresta-climb/.github/blob/main/LICENSE)**, e os metadados estruturados da base de dados de escalada sob a **Open Database License 1.0 (ODbL 1.0)**.

