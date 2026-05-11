# Primeiros Passos

Tudo que você precisa para sair do zero e ter o seu primeiro projeto funcionando no Sprickis.

---

<a id="criar-conta"></a>
## Criar conta

Acesse [sprickis.vercel.app](https://sprickis.vercel.app) e clique em **Criar conta** na landing page.

Você tem duas formas de se registrar:

**Com e-mail e senha**
1. Preencha nome, e-mail e senha (mínimo 8 caracteres)
2. Clique em **Criar conta**
3. Faça login com as credenciais que acabou de criar

**Com GitHub**
1. Clique em **Entrar com GitHub**
2. Autorize o acesso na tela do GitHub
3. Você será redirecionado automaticamente para o app

> Suas credenciais do GitHub usadas no login são separadas das permissões de integração de repositório. Entrar com GitHub dá acesso ao app; conectar um repositório a um projeto é um passo separado e opcional.

---

<a id="recuperar-senha"></a>
## Recuperar senha

Se você criou a conta com e-mail e senha e esqueceu a senha:

1. Na tela de login, clique em **Esqueci minha senha**
2. Informe o e-mail cadastrado
3. Você receberá um link de redefinição no e-mail (válido por tempo limitado)
4. Clique no link e defina a nova senha

---

<a id="criar-workspace"></a>
## Criar seu primeiro workspace

Um **workspace** é o seu ambiente de trabalho. Ele agrupa projetos e membros do seu time.

Ao criar sua conta e fazer login pela primeira vez, o Sprickis exibe a tela de criação de workspace automaticamente se você ainda não pertencer a nenhum.

Para criar um workspace:
1. Informe o **nome** do workspace (ex: "Time de Produto", "Meus Projetos")
2. Opcionalmente, adicione um **logo** (imagem)
3. Clique em **Criar workspace**

Você será o **Owner** deste workspace e terá controle total sobre ele.

---

<a id="criar-projeto"></a>
## Criar um projeto

Dentro do workspace, clique em **Novo projeto** no sidebar ou na página de projetos.

Ao criar um projeto, você define:
- **Nome** do projeto
- **Descrição** (opcional)
- **Slug** — identificador usado na URL (ex: `sprickis.vercel.app/projeto/meu-projeto`)
- **Repositório GitHub** — opcional, pode ser conectado depois na página de Integrações

O projeto criado já vem com colunas de kanban padrão: **Backlog**, **A fazer**, **Em progresso**, **Em revisão** e **Concluído**. Você pode criar, renomear, reordenar e excluir colunas nas configurações do projeto.

**NOTA:** Excluir colunas padrão vai afetar o funcionamento de funcionalidades da plataforma.

---

<a id="criar-sprint"></a>
## Criar um sprint

Sprints organizam tarefas em ciclos de trabalho com tempo definido.

Para criar um sprint:
1. Abra o projeto e vá para a aba **Kanban**
2. Clique em **Sprints** para abrir o modal **Gerenciar sprints**
3. No modal, clique em **Novo sprint**
4. Defina o nome, data de início e data de término
5. Clique em **Salvar**

Para **ativar** um sprint, abra o modal de gerenciamento de sprints e clique em **Ativar** no sprint desejado. Apenas um sprint pode estar ativo por vez em cada projeto.

O kanban pode exibir **Todas as tarefas** (sem filtro de sprint) ou somente as tarefas de um sprint específico. Use o seletor no topo do board para alternar.

---

<a id="criar-tarefa"></a>
## Criar a primeira tarefa

Com o projeto aberto no Kanban:

**Criação rápida (inline):**
1. No rodapé de qualquer coluna, clique em **+ Adicionar tarefa**
2. Digite o título e pressione **Enter** para salvar ou **Esc** para cancelar

**Criação com todos os campos:**
1. Abra qualquer tarefa existente ou clique em **+ Adicionar tarefa** em uma coluna
2. No drawer que abre, preencha os campos desejados (status, prioridade, responsável, sprint, estimativa, etc.)
3. As alterações são salvas automaticamente ao sair do campo

---

<a id="estrutura"></a>
## Entendendo a hierarquia

O Sprickis segue uma hierarquia clara:

```
Workspace
└── Projeto
    ├── Sprint
    │   └── Tarefa
    ├── Roadmap
    │   └── Fase
    └── Milestone
        └── Entregável
```

- **Workspace**: agrupa projetos e membros do time
- **Projeto**: unidade de trabalho com kanban, roadmap, milestones e integrações próprios
- **Sprint**: ciclo temporal de trabalho dentro de um projeto
- **Tarefa**: unidade mínima de trabalho, sempre vinculada a uma coluna e opcionalmente a um sprint
- **Fase (Roadmap)**: período estratégico no tempo, pode conter tarefas e ter dependências
- **Milestone**: marco formal de entrega, com entregáveis e responsáveis

---

<a id="proximos-passos"></a>
## Próximos passos

- [kanban.md](kanban.md) — como usar o board, filtros e drag and drop
- [tarefas.md](tarefas.md) — todos os campos e funcionalidades de uma tarefa
- [membros-permissoes.md](membros-permissoes.md) — convidar membros para o workspace
- [github.md](github.md) — conectar um repositório GitHub ao projeto
- [ia.md](ia.md) — gerar backlog automaticamente com IA
