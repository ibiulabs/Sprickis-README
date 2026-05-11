# Tarefas

Uma tarefa é a unidade mínima de trabalho no Sprickis. Ela vive no kanban de um projeto, dentro de uma coluna e opcionalmente vinculada a um sprint. Este documento descreve todos os campos e funcionalidades disponíveis no drawer de detalhe da tarefa.

---

<a id="abrir-drawer"></a>
## Abrir o detalhe

Clique em qualquer card do kanban para abrir o drawer de detalhe. O drawer abre como painel lateral sobre o board, sem redirecionar a página.

A URL é atualizada com `?task=[id]`, permitindo compartilhar o link direto para a tarefa.

---

<a id="campos"></a>
## Campos editáveis

<a id="titulo"></a>
### Título

O título da tarefa fica no topo do drawer. Clique nele para editar inline. A alteração é salva ao clicar fora do campo ou pressionar **Enter**.

<a id="descricao"></a>
### Descrição

Campo de texto livre abaixo do título. Clique em **Adicionar descrição** ou no campo existente para editar. Aceita quebras de linha. Salvo automaticamente ao sair do campo.

<a id="status-coluna"></a>
### Status (Coluna)

Controla em qual coluna do kanban a tarefa se encontra. Aparece como um seletor de status no drawer. Alterar o status é equivalente a mover o card de coluna manualmente.

<a id="prioridade"></a>
### Prioridade

Quatro níveis de prioridade:

| Valor | Cor no card |
|---|---|
| Crítica | Vermelho |
| Alta | Laranja |
| Média | Amarelo |
| Baixa | Azul |

<a id="responsavel"></a>
### Responsável

Um membro do workspace pode ser atribuído como responsável pela tarefa. Apenas membros que pertencem ao workspace são listados como opção.

<a id="sprint"></a>
### Sprint

Vínculo da tarefa com um sprint do projeto. A lista exibe os sprints disponíveis no projeto. A tarefa pode existir sem sprint.

<a id="estimativa"></a>
### Estimativa

Campo numérico com unidade configurável. As unidades disponíveis são: **horas** e **pontos**. Exemplo: `8 horas`, `5 pontos`.

<a id="etiquetas"></a>
### Etiquetas

Tags coloridas para categorizar tarefas. As etiquetas são criadas no nível do projeto e ficam disponíveis para todas as tarefas do projeto. Uma tarefa pode ter múltiplas etiquetas.

---

<a id="subtarefas"></a>
## Subtarefas

Divisão da tarefa principal em itens menores executáveis.

- Clique em **Adicionar subtarefa** para criar
- Cada subtarefa tem título e checkbox de conclusão
- O progresso das subtarefas (ex: `2/5`) é exibido no card do kanban
- Subtarefas podem ser reordenadas por drag and drop
- Cada conclusão de subtarefa gera um registro no histórico de atividade

---

<a id="checklist"></a>
## Checklist técnico

O checklist é uma lista de verificações de qualidade associadas à tarefa. Diferente das subtarefas, o checklist é focado em garantias técnicas (ex: "testes escritos", "revisão de código feita", "documentação atualizada").

Os itens de checklist podem ser organizados por **categorias**. As categorias são criadas dentro do drawer e agrupam os itens visualmente.

- Clique em **Adicionar item** para criar um item de checklist
- Clique em **+ Categoria** para criar uma categoria de agrupamento
- Marque o checkbox ao concluir cada item

> O checklist técnico também tem uma página dedicada no projeto (aba **Checklist**) que exibe o checklist consolidado de todas as tarefas do projeto.

---

<a id="comentarios"></a>
## Comentários

A aba **Comentários** no drawer exibe a thread de comentários da tarefa.

- Clique no campo de texto no rodapé da aba e escreva o comentário
- Pressione **Enviar** ou use **Ctrl+Enter** para publicar
- Comentários exibem o nome do autor, avatar e tempo relativo (ex: "há 3 horas")
- O envio de um comentário gera um registro no histórico de atividade

---

<a id="historico"></a>
## Histórico de atividade

A aba **Atividade** exibe o log cronológico de todas as ações realizadas nesta tarefa, incluindo:

- Criação da tarefa
- Alterações de status, prioridade, responsável, sprint e estimativa
- Adição e remoção de etiquetas
- Adição de comentários
- Conclusão de subtarefas
- Conclusão de itens de checklist
- Adição e remoção de dependências
- Vínculos com PRs e branches do GitHub

Cada entrada exibe o ator, a ação em português e o tempo relativo.

---

<a id="dependencias"></a>
## Dependências

Uma tarefa pode ser configurada como **bloqueante** de outra tarefa ou como **bloqueada** por outra.

- **Esta tarefa bloqueia**: a tarefa atual impede o andamento de outra
- **Esta tarefa é bloqueada por**: outra tarefa deve ser concluída antes desta
- **A conclusão de uma tarefa::** acontece quando uma tarefa tem as subtarefas marcadas como concluídas direto no drawer ou na aba **"Checklist"**.

Para vincular uma dependência para uma tarefa abra o drawer e insira em **"Dependências"** a tarefa que deve ser finalizada primeiro. 


Tarefas bloqueadas exibem um ícone de cadeado no card do kanban. As dependências são visíveis no drawer e geram registros no histórico de atividade.

---

<a id="vinculos-github"></a>
## Vínculos com GitHub

Se o projeto tiver integração com GitHub, o drawer exibe a seção **GitHub** com:

- **Pull Requests vinculados**: PRs associados a esta tarefa com número, título e status (aberto, mesclado, fechado)
- **Issues vinculadas**: issues do GitHub associadas
- **Branch vinculada**: branch criada especificamente para esta tarefa
- **Status de CI/CD**: status dos checks de CI do PR vinculado (pendente, passou, falhou)
- **Resumo de PR por IA**: botão para gerar automaticamente um resumo do PR usando IA

Para conectar um PR manualmente, clique em **Vincular PR** e informe o número do PR.

O webhook do GitHub pode automatizar esse vínculo se o título do commit ou PR seguir a convenção `[TASK-8 primeiros caracteres da task no sprickis]`.

---

<a id="excluir-tarefa"></a>
## Excluir tarefa

O botão de exclusão fica no menu de ações do drawer (ícone de lixeira). A exclusão é permanente e não pode ser desfeita. Confirme a ação no modal de confirmação antes de concluir.

Papéis que podem excluir tarefas: **Owner**, **Admin**, **Lead** e **Developer**. **Viewer** não pode excluir.
