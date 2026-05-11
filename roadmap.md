# Roadmap

O roadmap é a visão estratégica do projeto ao longo do tempo. Ele organiza o trabalho em **fases** posicionadas em uma linha do tempo horizontal, mostrando quando cada parte do projeto acontece, qual o progresso atual e quais fases dependem de outras.

---

<a id="acesso"></a>
## Acessar o roadmap

Na barra de navegação do projeto, clique em **Roadmap**.

---

<a id="linha-do-tempo"></a>
## Linha do tempo

O roadmap exibe uma timeline horizontal com as fases posicionadas de acordo com suas datas de início e término. O eixo horizontal representa o tempo (dias/semanas). Cada fase é exibida como uma barra horizontal.

A linha do tempo se ajusta automaticamente ao intervalo das fases criadas. Uma linha vertical indica a data atual.

---

<a id="fases"></a>
## Fases

Uma fase representa um período de trabalho com escopo, objetivo e prazo definidos. Exemplos: "MVP", "Beta", "Lançamento", "Sprint de performance".

<a id="criar-fase"></a>
### Criar fase

Clique em **Nova fase** para abrir o painel de criação. Informe:

- **Nome** da fase
- **Data de início**
- **Data de término**
- **Cor** (para diferenciar visualmente na timeline)
- **Descrição** (opcional)
- **Milestone vinculado** (opcional) — associa a fase a um marco de entrega

<a id="editar-fase"></a>
### Editar fase

Clique em uma fase na timeline ou no painel lateral para abrir seus detalhes. Todos os campos são editáveis.

<a id="progresso-da-fase"></a>
### Progresso automático da fase

O progresso de cada fase é calculado automaticamente com base nas tarefas do kanban vinculadas a ela:

```
progresso = tarefas na coluna "Done" ÷ total de tarefas vinculadas
```

Uma barra de progresso é exibida dentro da barra da fase na timeline.

Para vincular tarefas a uma fase, abra o detalhe da fase e use a seção **Tarefas** para buscar e adicionar tarefas do projeto.

<a id="vincular-milestone"></a>
### Vincular a um milestone

Uma fase pode ser vinculada a um milestone. O milestone aparece como um marcador na timeline e o progresso da fase contribui para o progresso consolidado do milestone.

---

<a id="dependencias"></a>
## Dependências entre fases

Uma fase pode depender de outra, o que significa que ela não deve ser iniciada até que a fase predecessora seja concluída.

Para adicionar uma dependência:
1. Abra o detalhe da fase
2. Na seção **Dependências**, busque a fase bloqueante e clique em **Adicionar**

As dependências são exibidas visualmente na timeline como setas ou linhas de conexão entre as fases.

Tipos de dependência:
- **Esta fase bloqueia**: a fase atual deve ser concluída antes que outra comece
- **Esta fase é bloqueada por**: outra fase deve ser concluída antes desta começar

---

<a id="detalhe-da-fase"></a>
## Painel de detalhe da fase

Clicar em uma fase abre o painel lateral com:

- **Dados gerais**: nome, datas, cor, descrição
- **Milestone vinculado**: nome do milestone associado (se houver)
- **Tarefas vinculadas**: lista de tarefas do kanban associadas à fase, com status de cada uma
- **Dependências**: fases que bloqueiam ou são bloqueadas por esta
- **Progresso**: porcentagem calculada automaticamente

A URL é atualizada com `?phase=[id]`, permitindo compartilhar o link direto para uma fase.

---

<a id="excluir-fase"></a>
## Excluir fase

No painel de detalhe da fase, clique no menu de ações e selecione **Excluir**. A exclusão remove a fase e seus vínculos com tarefas e milestones. As tarefas em si não são excluídas.

Somente **Owner**, **Admin** e **Lead** podem excluir fases. **Developer** e **Viewer** não podem.
