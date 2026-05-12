# Sprickis

> **Construa software sprint após sprint.**

Plataforma de gestão de projetos de software para times técnicos. Acesse em [sprickis.vercel.app](https://sprickis.vercel.app) — gratuito, sem cartão de crédito, sem planos pagos.

---

<a id="o-que-e"></a>
## O que é o Sprickis

O Sprickis é uma plataforma web de gestão de projetos construída especificamente para times de desenvolvimento de software. Ele reúne em um único lugar o que normalmente está espalhado por várias ferramentas: kanban para execução diária, roadmap para visão estratégica, milestones para marcos formais de entrega, checklists técnicos por tarefa e integração real com GitHub.

O produto funciona como um cockpit de desenvolvimento. Um ambiente único onde o time planeja, executa, acompanha e evolui projetos com clareza e rastreabilidade completa — da tarefa de hoje ao milestone do próximo trimestre.

A hierarquia é simples e rígida: **Workspace → Projeto → Sprint → Tarefa**. Um workspace agrupa projetos e membros. Cada projeto tem seu próprio kanban, roadmap, milestones e integrações. As tarefas vivem dentro de sprints e colunas configuráveis.

---

<a id="por-que-foi-criado"></a>
## Por que foi criado

O Sprickis é um projeto 100% sem fins lucrativos criado pelo fundador da [ibiulabs](https://github.com/ibiulabs) para resolver seus próprios problemas de gestão de projetos de software.

Ferramentas existentes eram genéricas demais (Notion, Trello), complexas demais (Jira) ou caras demais para times pequenos. O Sprickis foi construído para o problema real: um time técnico pequeno que precisa de estrutura séria sem overhead burocrático.

O uso é completamente livre. Sem planos pagos. Sem limitações por tier. Sem anúncios. Sem coleta de dados para venda. O código não é open source — não aceita contribuições externas — mas a plataforma existe para ser usada por qualquer desenvolvedor ou time que se beneficiar dela.

---

<a id="como-foi-construido"></a>
## Como foi construído

O Sprickis foi desenvolvido com uma abordagem de **Spec-Driven Development (SDD)**: toda a documentação técnica foi escrita antes do código. Schema do banco, fluxo de autenticação, hierarquia de permissões, comportamento de cada rota de API — tudo especificado em markdown antes de qualquer linha de TypeScript.

A IA foi usada como ferramenta de implementação supervisionada por engenharia real. As decisões de arquitetura, modelagem de dados e segurança foram humanas; a IA acelerou a escrita do código dentro dessas decisões.

O SQL é escrito diretamente no repositório via Drizzle ORM — migrations versionadas, sem magia de ORM que esconde o que está acontecendo no banco. As variáveis de ambiente de produção são protegidas como `sensitive` na Vercel. O código passou por auditoria de segurança antes do lançamento público, cobrindo autenticação, autorização, injeção de dados, headers HTTP e dependências.

---

<a id="funcionalidades"></a>
## Funcionalidades

| Funcionalidade | Descrição |
|---|---|
| **Kanban** | Board com colunas configuráveis, drag and drop, filtros, sprints e criação rápida de tarefas inline |
| **Detalhe de tarefa** | Drawer lateral com todos os campos editáveis, subtarefas, checklist técnico, comentários, histórico de atividade e vínculos GitHub |
| **Roadmap** | Linha do tempo com fases, dependências entre fases, progresso automático e vínculo com milestones |
| **Milestones** | Marcos formais de entrega com entregáveis, responsáveis, progresso automático e geração de sprints por IA |
| **Checklist técnico** | Checklist por categoria dentro de cada tarefa para garantir qualidade de entrega |
| **Sprints** | Criação, ativação e conclusão de sprints por projeto; alternância no kanban |
| **Integração GitHub** | Conectar repositório via OAuth, sincronizar PRs e issues, automação de status via webhook, status de CI/CD nos cards |
| **IA — Geração de backlog** | Gerar tarefas, milestones e fases de roadmap a partir de uma descrição em texto livre |
| **IA — Contexto do repositório** | Gerar o projeto inteiro usando o contexto real do repositório GitHub conectado (aceita também um prompt adicional) |
| **IA — Resumo de PR** | Resumo automático do pull request gerado por IA no detalhe da tarefa |
| **IA — Previsão de sprints** | Estimativa de velocidade do time e previsão de conclusão de sprints |
| **Membros e permissões** | 5 papéis (Owner, Admin, Lead, Developer, Viewer) com controle granular por ação |
| **Convites por e-mail** | Convidar membros por e-mail com link de aceite com expiração |
| **Histórico de atividade** | Log completo de todas as ações realizadas no projeto |
| **Múltiplos workspaces** | Pertencer a múltiplos workspaces e alternar entre eles pelo sidebar |
| **Busca rápida** | Paleta de comandos global (Ctrl+K / Cmd+K) para navegar entre projetos e tarefas |
| **Dashboard** | Visão consolidada do projeto com progresso, tarefas críticas, sprint atual e milestones próximos |

---

<a id="tecnologias"></a>
## Tecnologias utilizadas

| Tecnologia | Versão | Papel |
|---|---|---|
| **Next.js** | 15.3.2 | Base full-stack com App Router e Route Handlers |
| **React** | 19.1.0 | Interface declarativa |
| **TypeScript** | 5.8.3 | Tipagem estrita em todo o projeto |
| **Tailwind CSS** | 4.1.8 | Estilização |
| **Shadcn/UI** | — | Componentes base |
| **Drizzle ORM** | 0.45.2 | Schema, migrations e queries tipadas |
| **PostgreSQL / Neon** | — | Banco de dados serverless |
| **NextAuth.js** | 5.0.0-beta.28 | Autenticação (credentials + GitHub OAuth) |
| **Vercel** | — | Hospedagem e deploy contínuo |
| **Brevo** | — | E-mails transacionais (convites, recuperação de senha) |
| **dnd-kit** | 6.3.1 (core) / 10.0.0 (sortable) | Drag and drop do kanban |
| **Zustand** | 5.0.5 | Estado global do cliente |
| **Zod** | 3.25.36 | Validação de schemas em formulários e APIs |
| **TanStack Query** | 5.76.1 | Cache e sincronização de dados do servidor |
| **Google Gemini** | 0.24.1 (@google/generative-ai) | Modelo de IA para geração de backlog e resumos |
| **date-fns** | 4.1.0 | Manipulação de datas |
| **React Hook Form** | 7.56.3 | Gerenciamento de formulários |
| **bcryptjs** | 3.0.2 | Hash de senhas |

---

<a id="numeros"></a>
## Números do projeto

| Métrica | Valor |
|---|---|
| Linhas de TypeScript/TSX | **23.938** |
| Linhas de documentação Markdown | **2.357** |
| Arquivos TypeScript/TSX | **214** |

---

<a id="documentacao"></a>
## Documentação

| Arquivo | Conteúdo |
|---|---|
| [primeiros-passos.md](primeiros-passos.md) | Criar conta, workspace, projeto e primeira tarefa |
| [kanban.md](kanban.md) | Board kanban, sprints, filtros, drag and drop |
| [tarefas.md](tarefas.md) | Detalhe completo de tarefa, todos os campos e funcionalidades |
| [roadmap.md](roadmap.md) | Linha do tempo, fases, dependências, progresso |
| [milestones.md](milestones.md) | Marcos de entrega, entregáveis, geração de sprints por IA |
| [github.md](github.md) | Conectar repositório, sincronização, webhook, CI/CD |
| [ia.md](ia.md) | Geração de backlog, resumo de PR, previsão de sprints |
| [membros-permissoes.md](membros-permissoes.md) | Papéis, matriz de permissões, convites |
| [configuracoes.md](configuracoes.md) | Configurações de workspace, projeto e colunas do kanban |

---

<a id="acesso"></a>
## Acesso

A plataforma está disponível em **[sprickis.vercel.app](https://sprickis.vercel.app)**.

O uso é gratuito e sem restrições. Não é necessário cartão de crédito. Basta criar uma conta com e-mail e senha ou entrar com GitHub.
