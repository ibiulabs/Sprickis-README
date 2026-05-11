# Milestones

Milestones são marcos formais de entrega de um projeto. Eles representam momentos significativos — como o lançamento de uma versão, a entrega de um módulo ou a conclusão de uma fase de desenvolvimento — e reúnem entregáveis, responsáveis e tarefas em um único ponto de referência.

---

<a id="acesso"></a>
## Acessar os milestones

Na barra de navegação do projeto, clique em **Milestones**.

---

<a id="lista-de-milestones"></a>
## Lista de milestones

A página exibe todos os milestones do projeto ordenados por data de entrega. Cada card de milestone mostra:

- Nome e data de entrega
- Progresso (porcentagem de tarefas concluídas)
- Responsáveis atribuídos
- Número de entregáveis e seu status

---

<a id="criar-milestone"></a>
## Criar milestone

Clique em **Novo milestone** para abrir o modal de criação. Informe:

- **Nome** do milestone
- **Data de entrega** (due date)
- **Descrição** (opcional)

---

<a id="detalhe-do-milestone"></a>
## Painel de detalhe

Clique em um milestone para abrir seu painel de detalhe. A URL é atualizada com `?milestone=[id]`.

O painel exibe e permite editar:

<a id="entregaveis"></a>
### Entregáveis

Entregáveis são os itens concretos que devem ser produzidos ou concluídos para que o milestone seja considerado encerrado. Exemplos: "Documentação publicada", "Deploy em produção", "Aprovação do cliente".

- Clique em **+ Entregável** para adicionar
- Cada entregável tem um título e um checkbox de conclusão
- Os entregáveis podem ser reordenados por drag and drop

<a id="tarefas-do-milestone"></a>
### Tarefas vinculadas

Tarefas do kanban podem ser associadas ao milestone. A conclusão das tarefas é usada para calcular o progresso do milestone.

- Use a busca de tarefas no painel para encontrar e vincular tarefas existentes do projeto
- O progresso exibido no card do milestone é calculado como:

```
progresso = tarefas na coluna "Done" ÷ total de tarefas vinculadas
```

<a id="responsaveis"></a>
### Responsáveis

Membros do workspace podem ser atribuídos como responsáveis pelo milestone. Responsáveis são exibidos nos cards da lista.

<a id="fases-do-roadmap"></a>
### Fases do roadmap vinculadas

Fases do roadmap que estão vinculadas a este milestone aparecem no painel. O vínculo é criado nas configurações de cada fase (ver [roadmap.md](roadmap.md)).

---

<a id="progresso-automatico"></a>
## Progresso automático

O progresso de cada milestone é calculado em tempo real com base nas tarefas vinculadas a ele:

- Tarefas na coluna marcada como "Done" no projeto contribuem como `concluídas`
- O percentual é exibido como barra de progresso no card e no painel de detalhe

Se nenhuma tarefa estiver vinculada, o progresso é baseado nos entregáveis marcados como concluídos.

---

<a id="ia-sprint"></a>
## Gerar sprint por IA a partir de um milestone

A partir do painel de um milestone, você pode solicitar à IA que gere automaticamente um sprint com as tarefas necessárias para cumprir aquele marco.

1. No painel do milestone, clique em **Gerar sprint com IA**
2. A IA analisa o nome, descrição e entregáveis do milestone
3. Um sprint com tarefas sugeridas é criado no projeto para revisão
4. Revise, ajuste e ative o sprint gerado

Esta funcionalidade requer que o usuário tenha papel de **Owner**, **Admin** ou **Lead** no workspace.

---

<a id="excluir-milestone"></a>
## Excluir milestone

No painel de detalhe, clique em **Excluir milestone**. A exclusão remove o milestone, seus entregáveis e vínculos com tarefas. As tarefas em si não são excluídas.

Somente **Owner**, **Admin** e **Lead** podem excluir milestones.
