# Membros e Permissões

O controle de acesso no Sprickis é baseado em papéis (roles) atribuídos por workspace. Cada membro de um workspace tem exatamente um papel, e esse papel determina o que ele pode ver e fazer em todos os projetos daquele workspace.

---

<a id="papeis"></a>
## Papéis disponíveis

| Papel | Descrição |
|---|---|
| **Owner** | Criador do workspace. Controle total. Só ele pode deletar o workspace. Não pode ser removido. |
| **Admin** | Gerencia membros, cria e deleta projetos, altera configurações do workspace. |
| **Lead** | Organiza roadmap, milestones, sprints e fluxo de entrega. Pode criar e editar tarefas de qualquer membro. |
| **Developer** | Executa tarefas atribuídas a ele, atualiza cards, preenche checklists, abre comentários. |
| **Viewer** | Acesso de apenas leitura. Não pode criar, editar ou mover nada. |

---

<a id="matriz-de-permissoes"></a>
## Matriz de permissões

| Ação | Owner | Admin | Lead | Developer | Viewer |
|---|:---:|:---:|:---:|:---:|:---:|
| Deletar workspace | ✅ | ❌ | ❌ | ❌ | ❌ |
| Gerenciar membros | ✅ | ✅ | ❌ | ❌ | ❌ |
| Criar projeto | ✅ | ✅ | ❌ | ❌ | ❌ |
| Deletar projeto | ✅ | ✅ | ❌ | ❌ | ❌ |
| Gerenciar roadmap | ✅ | ✅ | ✅ | ❌ | ❌ |
| Gerenciar milestones | ✅ | ✅ | ✅ | ❌ | ❌ |
| Criar sprint | ✅ | ✅ | ✅ | ❌ | ❌ |
| Criar tarefa | ✅ | ✅ | ✅ | ✅ | ❌ |
| Editar qualquer tarefa | ✅ | ✅ | ✅ | ❌ | ❌ |
| Editar própria tarefa | ✅ | ✅ | ✅ | ✅ | ❌ |
| Mover tarefa no kanban | ✅ | ✅ | ✅ | ✅ | ❌ |
| Preencher checklist | ✅ | ✅ | ✅ | ✅ | ❌ |
| Comentar em tarefa | ✅ | ✅ | ✅ | ✅ | ❌ |
| Acessar funcionalidades de IA | ✅ | ✅ | ✅ | ✅ | ❌ |
| Conectar/desconectar GitHub | ✅ | ✅ | ❌ | ❌ | ❌ |
| Visualizar tudo | ✅ | ✅ | ✅ | ✅ | ✅ |

---

<a id="pagina-de-membros"></a>
## Página de Membros

Na barra lateral, clique em **Membros** dentro do workspace (não dentro de um projeto — é uma página do workspace).

A página exibe:
- Lista de todos os membros ativos, ordenados com o Owner no topo e demais por data de entrada
- Nome, e-mail, avatar e papel de cada membro
- Convites pendentes (visível apenas para Owner e Admin)

---

<a id="convidar-membro"></a>
## Convidar novo membro

Somente **Owner** e **Admin** podem convidar membros.

1. Na página de Membros, clique em **Convidar membro**
2. Informe o **e-mail** do convidado
3. Selecione o **papel** que será atribuído ao membro ao aceitar
4. Clique em **Enviar convite**

O Sprickis envia um e-mail para o endereço informado com um link de aceite. O link tem validade de **7 dias**. Após expirar, o convite é descartado e um novo precisa ser enviado.

Convites pendentes aparecem na seção **Convites pendentes** da página de membros, com o e-mail do convidado, papel atribuído, nome do quem convidou e data de criação.

---

<a id="aceitar-convite"></a>
## Aceitar um convite

O link de convite recebido por e-mail pode ser acessado por qualquer pessoa:

- **Se o e-mail já tem conta**: faça login e o workspace é adicionado automaticamente ao seu perfil
- **Se o e-mail não tem conta**: você será direcionado para criar uma conta com aquele e-mail antes de aceitar

Após aceitar, o membro passa a aparecer na lista com o papel que foi atribuído no convite.

---

<a id="alterar-papel"></a>
## Alterar o papel de um membro

Na página de Membros, clique no papel de um membro para abrir o seletor. Selecione o novo papel e confirme.

Somente **Owner** e **Admin** podem alterar papéis. O Owner não pode ter seu próprio papel alterado.

---

<a id="remover-membro"></a>
## Remover membro

Na página de Membros, passe o mouse sobre um membro e clique no ícone de remoção. Confirme no modal.

Regras:
- **Owner** pode remover qualquer membro
- **Admin** pode remover membros com papel inferior ao seu (não pode remover outro Admin ou o Owner)
- O **Owner** não pode ser removido do workspace

Ao remover um membro, ele perde imediatamente o acesso ao workspace e a todos os seus projetos. As tarefas atribuídas a ele permanecem no kanban — apenas o responsável pode ser reatribuído.

---

<a id="multiplos-workspaces"></a>
## Pertencer a múltiplos workspaces

Um usuário pode pertencer a quantos workspaces quiser, com papéis diferentes em cada um. O workspace ativo é exibido no topo do sidebar.

Para alternar entre workspaces, clique no nome do workspace no sidebar e selecione outro da lista, ou use a opção **Mudar workspace**.

O workspace ativo é mantido em cookie de sessão — ao reabrir o Sprickis, você retorna para o último workspace utilizado.
