# Kanban

O kanban é a principal tela de trabalho diário dentro de um projeto. É onde tarefas são criadas, movidas entre colunas, filtradas por sprint e gerenciadas em detalhe.

---

<a id="navegacao"></a>
## Acessar o kanban

Na barra lateral esquerda, selecione o projeto desejado. O kanban é exibido na aba **Kanban** da navegação do projeto.

---

<a id="colunas"></a>
## Colunas

O kanban de cada projeto tem colunas configuráveis. As colunas padrão criadas com cada projeto são:

| Coluna | Tipo |
|---|---|
| Backlog | Normal |
| A fazer | Normal |
| Em progresso | Normal |
| Em revisão | Normal |
| Concluído | Coluna de conclusão (Done) |

As colunas podem ser criadas, renomeadas, reordenadas e excluídas nas **Configurações do projeto**. A coluna marcada como "Done" é usada pelo sistema para calcular progresso no roadmap e milestones automaticamente.

---

<a id="drag-and-drop"></a>
## Drag and drop

Para mover uma tarefa entre colunas, arraste o card e solte-o na coluna de destino. O sistema atualiza o status imediatamente e persiste no banco com rollback automático em caso de falha de rede.

Para reordenar tarefas dentro de uma mesma coluna, arraste o card para cima ou para baixo.

O drag and drop utiliza a biblioteca **dnd-kit** com sensor de ponteiro (mínimo de 5px de deslocamento para ativar o drag, evitando cliques acidentais).

---

<a id="sprints"></a>
## Sprints

<a id="selecionar-sprint"></a>
### Selecionar sprint

O seletor de sprint fica no topo esquerdo do board. As opções são:

- **Todos os sprints** — exibe tarefas de todos os sprints (e tarefas sem sprint)
- **[Nome do sprint]** — filtra o board para exibir somente as tarefas do sprint selecionado

O sprint ativo do projeto é selecionado automaticamente quando você abre o kanban. Se não houver sprint ativo, o board inicia em "Todos os sprints".

<a id="gerenciar-sprints"></a>
### Gerenciar sprints

Clique no botão ao lado do seletor de sprint e selecione para **Gerenciar sprints** para abrir o modal de gestão.

No modal você pode:
- **Criar** um novo sprint (nome, data de início, data de término)
- **Editar** nome e datas de um sprint existente
- **Ativar** um sprint (somente um ativo por vez)
- **Concluir** o sprint ativo
- **Excluir** um sprint (as tarefas permanecem no projeto, apenas perdem o vínculo com o sprint)

---

<a id="filtros"></a>
## Filtros

O kanban tem filtros disponíveis no topo do board, representados pelo ícone de filtros:

| Filtro | O que faz |
|---|---|
| **Responsável** | Exibe apenas tarefas atribuídas ao membro selecionado |
| **Prioridade** | Exibe apenas tarefas com a prioridade selecionada (Crítica, Alta, Média, Baixa) |
| **Busca por título** | Filtra tarefas que contenham o texto digitado no título |
| **Sem sprint** | Exibe apenas tarefas que não estão em nenhum sprint |
| **Sem responsável** | Exibe apenas tarefas sem responsável atribuído |
| **Estagnadas** | Exibe apenas tarefas sem atualização há mais de 7 dias |

Múltiplos filtros podem ser aplicados simultaneamente. Os filtros afetam apenas a visualização — nenhuma tarefa é deletada ou movida.

A barra de busca por título fica visível no topo do board (ícone de lupa).

---

<a id="criar-tarefa-inline"></a>
## Criar tarefa diretamente no board

No topo de cada coluna há um botão **+ Adicionar tarefa**. Ao clicar:

1. Um campo de texto aparece no final da coluna
2. Digite o título da tarefa e pressione **Enter** para criar
3. Pressione **Esc** para cancelar

A tarefa é criada com a coluna atual, sem sprint vinculado. Para preencher os demais campos (prioridade, responsável, sprint etc.), abra o drawer da tarefa clicando nela.

Se o projeto tiver **integração GitHub ativa**, ao criar uma tarefa diretamente no board você verá uma opção para criar automaticamente uma issue no GitHub vinculada a essa tarefa.

---

<a id="abrir-tarefa"></a>
## Abrir o detalhe da tarefa

Clique em qualquer card do kanban para abrir o drawer de detalhe da tarefa. O drawer abre sobre o board sem redirecionar a página.

A URL é atualizada com o parâmetro `?task=[id]`, permitindo compartilhar o link direto para uma tarefa específica.

Para fechar o drawer, clique no **X** no canto superior direito do drawer ou pressione **Esc**.

Para todos os campos e funcionalidades disponíveis no detalhe da tarefa, consulte [tarefas.md](tarefas.md).

---

<a id="configuracoes-de-coluna"></a>
## Configurar colunas

Para criar, renomear, reordenar ou excluir colunas, acesse **Configurações** do projeto na barra de navegação e veja a seção de colunas. Consulte [configuracoes.md](configuracoes.md) para detalhes.
