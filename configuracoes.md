# Configurações

Este documento cobre as configurações disponíveis para workspace, projeto e colunas do kanban.

---

<a id="configuracoes-do-workspace"></a>
## Configurações do Workspace

Acesse pelo sidebar: clique em **Configurações** dentro do workspace (não dentro de um projeto).

Somente **Owner** e **Admin** podem acessar as configurações do workspace.

<a id="info-do-workspace"></a>
### Informações gerais

| Campo | O que faz |
|---|---|
| **Nome** | Nome exibido no sidebar e na interface. Pode ser alterado a qualquer momento. |
| **Slug** | Identificador usado na URL (`sprickis.vercel.app/workspace/[slug]`). Alterar o slug rediirecionará para a nova URL. |
| **Logo** | URL de imagem exibida no topo do sidebar como avatar do workspace. |

Clique em **Salvar** para persistir as alterações.

<a id="deletar-workspace"></a>
### Deletar workspace

Na seção **Zona de perigo** das configurações do workspace, o Owner pode deletar permanentemente o workspace.

Para confirmar:
1. Digite o nome exato do workspace no campo de confirmação
2. Clique em **Deletar workspace**

A exclusão é irreversível. Todos os projetos, tarefas, sprints, roadmap, milestones, membros e dados associados são excluídos permanentemente.

Somente o **Owner** pode deletar o workspace. Admin e demais papéis não têm acesso a esta ação.

---

<a id="configuracoes-do-projeto"></a>
## Configurações do Projeto

Dentro do projeto, clique em **Configurações** na barra de navegação.

Somente **Owner** e **Admin** podem alterar as configurações do projeto. **Lead** tem acesso de leitura mas não pode salvar alterações.

<a id="info-do-projeto"></a>
### Informações gerais

| Campo | O que faz |
|---|---|
| **Nome** | Nome do projeto exibido no sidebar e no título das páginas. |
| **Slug** | Identificador usado na URL do projeto (`/projeto/[slug]`). Alterar o slug redireciona automaticamente para a nova URL. |
| **Descrição** | Texto descritivo do projeto (exibido no dashboard e na listagem). |

Ao alterar o nome, o slug é sugerido automaticamente com base no novo nome. Você pode editar o slug manualmente.

Clique em **Salvar** para persistir as alterações de informações gerais.

<a id="colunas-do-kanban"></a>
### Colunas do Kanban

A seção de colunas exibe todas as colunas do projeto com opções para gerenciá-las.

**Criar coluna:**
1. No final da lista de colunas, clique em **+ Adicionar coluna**
2. Informe o nome
3. Clique em salvar

**Editar coluna:**
- Clique no nome da coluna para editar inline
- Marque/desmarque o toggle **Done** para indicar se a coluna representa conclusão de tarefa

> A coluna marcada como **Done** é usada para calcular progresso automático no roadmap e milestones. Deve existir exatamente uma coluna Done por projeto para que o progresso funcione corretamente.

**Reordenar colunas:**
- Arraste as linhas de coluna pela alça de arrasto para reorganizar a ordem de exibição no kanban

**Excluir coluna:**
- Clique no ícone de lixeira ao lado da coluna
- Confirme a exclusão no modal

> Não é possível excluir uma coluna que tenha tarefas. Mova ou exclua as tarefas antes de remover a coluna.

<a id="deletar-projeto"></a>
### Deletar projeto

Na seção **Zona de perigo** das configurações do projeto:
1. Digite o nome exato do projeto no campo de confirmação
2. Clique em **Deletar projeto**

A exclusão é irreversível e remove todas as tarefas, sprints, roadmap, milestones e dados associados ao projeto.

Somente **Owner** e **Admin** podem deletar projetos.

---

<a id="configuracoes-de-conta"></a>
## Configurações de conta

Acesse pelo sidebar clicando no seu avatar ou nome, e selecionando **Conta**.

Na página de conta você pode alterar:
- **Nome** exibido na plataforma
- **Foto de perfil** (URL de imagem)
- **Senha** (somente para contas criadas com e-mail e senha — contas GitHub usam o provedor externo)
