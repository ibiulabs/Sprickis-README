# Inteligência Artificial

O Sprickis integra IA em três pontos do fluxo de desenvolvimento: geração de backlog a partir de texto, geração de backlog a partir do contexto de um repositório GitHub e análise preditiva de velocidade do time.

O modelo utilizado é o **Gemini** (Google) via a biblioteca `@google/generative-ai`.

---

<a id="quem-pode-usar"></a>
## Quem pode usar

Todas as funcionalidades de IA requerem que o usuário tenha papel de **Owner**, **Admin**, **Lead** ou **Developer** no workspace. **Viewer** não tem acesso à página de IA.

---

<a id="gerar-backlog-com-texto"></a>
## Gerar backlog com texto

A funcionalidade principal de IA gera tarefas, milestones e fases de roadmap a partir de uma descrição em linguagem natural.

### Acessar

Na navegação do projeto, clique em **IA** para abrir a página **Gerar Backlog com IA**.

### Como usar

1. No campo de texto, descreva a feature, objetivo ou projeto que deseja planejar
   - Exemplo: *"Precisamos de um sistema de notificações em tempo real para alertar usuários sobre novas mensagens, comentários em tarefas e menções"*
2. Clique em **Gerar**
3. A IA processa a descrição e retorna sugestões em três abas:

| Aba | Conteúdo gerado |
|---|---|
| **Tarefas** | Lista de tarefas com título, descrição, prioridade, estimativa, etiquetas, subtarefas e checklist técnico |
| **Milestones** | Marcos de entrega sugeridos com nome, objetivo e prazo relativo em dias |
| **Fases** | Fases de roadmap sugeridas com nome, objetivo e duração em dias |

### Revisar e importar

Na aba **Tarefas**, você pode:
- Marcar e desmarcar tarefas individualmente para selecionar quais importar
- Expandir cada tarefa para ver subtarefas e checklist gerados
- Usar **Selecionar todas** / **Desmarcar todas**

Clique em **Importar selecionadas** para criar as tarefas escolhidas no projeto. As tarefas são criadas no Backlog.

As abas de Milestones e Fases exibem as sugestões para referência. A importação automática dessas para o sistema é feita manualmente — use as sugestões como guia para criar os milestones e fases pelo roadmap e milestones normalmente.

### Limite de tamanho

A descrição aceita no máximo **4.000 caracteres**. Descrições maiores retornam erro antes de enviar para a IA.

---

<a id="gerar-a-partir-do-repositorio"></a>
## Gerar projeto a partir do repositório GitHub

Quando o projeto tem integração com GitHub ativa, há uma segunda opção de geração: usar o contexto real do repositório conectado.

### Como usar

1. Abra a página **Integrações** do projeto (requer integração GitHub ativa)
2. Selecione a opção **Gerar projeto com IA**
3. Clique em **Gerar**

A IA consulta a estrutura do repositório (arquivos, dependências, README, código) para gerar sugestões de projeto completo contextualmente relevantes ao que já existe no projeto.

O resultado é apresentado nas mesmas três abas (Kanban, Milestones, Fases) e importado da mesma forma.

---

<a id="resumo-de-pr"></a>
## Resumo de Pull Request por IA

No drawer de detalhe de uma tarefa que tem um PR vinculado, há um botão **Resumo por IA** na seção GitHub.

Ao clicar:
1. A IA analisa o título, descrição e diff do PR vinculado
2. Um resumo em texto é gerado descrevendo o que foi alterado, o impacto e os pontos de atenção
3. O resumo aparece no drawer da tarefa

Esta funcionalidade é útil para revisores que precisam entender rapidamente o escopo de um PR antes de revisar o código.

---

<a id="previsao-de-velocidade"></a>
## Previsão de velocidade do time - Gerar sprints do milestone

A previsão de velocidade calcula quanto tempo o time levará para completar uma determinada quantidade de trabalho com base no histórico de sprints concluídos.

### Como funciona

O sistema analisa os sprints já concluídos do projeto e calcula:

- **Velocidade média**: média de pontos concluídos por sprint
- **Duração média de sprint**: média em dias dos sprints do projeto
- **Sprints necessários**: quantos sprints serão necessários para concluir os pontos informados
- **Data estimada de conclusão**: data calculada com base nos sprints necessários e na duração média

Se o projeto não tiver sprints suficientes concluídos para calcular a velocidade, o sistema usa valores padrão.

### Onde ver

A previsão de velocidade aparece na página de milestone, ao clicar em um milestone e em seguida "Gerar sprints".

---

<a id="qualidade-dos-resultados"></a>
## Qualidade dos resultados

Os resultados gerados pela IA são sugestões e devem ser revisados antes de serem importados. A qualidade melhora com descrições mais detalhadas e contextuais.

- Seja específico sobre tecnologias, domínio e objetivos
- Mencione restrições importantes (prazo, escopo, integrações necessárias)
- Você pode gerar múltiplas vezes com variações na descrição e comparar os resultados

A IA não tem acesso ao histórico de tarefas do projeto — ela trabalha somente com o texto fornecido e, quando aplicável, com o contexto do repositório GitHub conectado.
