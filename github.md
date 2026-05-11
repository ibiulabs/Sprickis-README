# Integração com GitHub

O Sprickis permite conectar um repositório GitHub a um projeto. A integração traz pull requests e issues do repositório para dentro da plataforma, automatiza vínculos entre código e tarefas, e exibe status de CI/CD diretamente nos cards do kanban.

---

<a id="pre-requisitos"></a>
## Pré-requisitos

- Você precisa ter uma conta GitHub
- O repositório pode ser público ou privado
- Para receber eventos em tempo real (webhook), o repositório precisa estar acessível pela internet (não é necessário para uso manual)

---

<a id="conectar-repositorio"></a>
## Conectar um repositório

1. Na navegação do projeto, clique em **Integrações**
2. Clique em **Conectar com GitHub**
3. Você será redirecionado para a tela de autorização do GitHub
4. Autorize o acesso e selecione o repositório desejado
5. Você retornará ao Sprickis com a integração configurada

A integração armazena somente o nome do repositório, do proprietário e o token de acesso necessário para consultas à API do GitHub. As credenciais são armazenadas de forma segura.

---

<a id="pagina-de-integracoes"></a>
## Página de integrações

Após conectar, a página **Integrações** exibe:

- **Status da integração**: conectado, sincronizando, desconectado
- **Repositório**: proprietário e nome (ex: `minha-org/meu-repo`)
- **Última sincronização**: data e hora da última sincronização
- **Configurações de sincronização** (ver abaixo)
- **Pull Requests**: lista dos últimos 50 PRs do repositório

---

<a id="pull-requests"></a>
## Pull Requests

A integração sincroniza os pull requests do repositório e os exibe na página de integrações. Cada PR mostra:

- Número e título
- Status: aberto, mesclado ou fechado
- Branch de origem e destino
- Data de atualização

Você pode vincular um PR a uma tarefa do kanban. O vínculo aparece no drawer da tarefa com o número, título e status do PR, incluindo status de CI/CD se disponível.

---

<a id="configuracoes-de-sincronizacao"></a>
## Configurações de sincronização

Na página de integrações, há dois toggles configuráveis:

| Configuração | O que faz |
|---|---|
| **Sincronizar issues** | Importa as issues abertas do repositório como tarefas no kanban |
| **Sincronização bidirecional** | Alterações de status nas tarefas do Sprickis são refletidas nas issues do GitHub, e vice-versa |

Alterações nessas configurações são salvas automaticamente.

---

<a id="webhook"></a>
## Webhook

O webhook permite que o GitHub notifique o Sprickis em tempo real quando eventos acontecem no repositório (PR aberto, PR mesclado, CI concluído, etc.).

Para configurar o webhook no repositório:

1. Na página de integrações do Sprickis, copie a **URL do webhook** e o **segredo do webhook**
2. No GitHub, vá para o repositório → **Settings** → **Webhooks** → **Add webhook**
3. Cole a URL no campo **Payload URL**
4. Selecione o tipo de conteúdo `application/json`
5. Cole o segredo no campo **Secret**
6. Selecione os eventos: **All events**
7. Clique em **Add webhook**

Após configurar, o Sprickis passará a receber eventos em tempo real e atualizará os vínculos de tarefas automaticamente.

---

<a id="automacao-via-mensagem-de-commit"></a>
## Automação via título de commit ou PR

Se o webhook estiver configurado, o Sprickis interpreta convenções nos títulos de PRs e commits para criar vínculos automaticamente.

| Convenção | Efeito |
|---|---|
| `[TASK-primeiros 8 caracteres da tarefa no sprickis]` | Vincula o commit ou PR à tarefa sprickis|

Onde `TASK` é o identificador interno da tarefa no Sprickis (visível na URL do drawer). Para conseguir os caracteres basta observar o que aparece depois de "task=" na URL da tarefa.

---

<a id="ci-cd"></a>
## Status de CI/CD

Quando um PR está vinculado a uma tarefa, o status dos checks de CI/CD do PR é exibido no drawer da tarefa:

- **Pendente**: checks em andamento
- **Passou**: todos os checks passaram
- **Falhou**: um ou mais checks falharam

O status é atualizado automaticamente quando o webhook está ativo.

---

<a id="desconectar"></a>
## Desconectar o repositório

Na página de integrações, clique em **Desconectar**. Confirme no modal.

A desconexão remove a integração, os dados de PR armazenados no cache e os vínculos entre PRs e tarefas. As tarefas em si não são afetadas.

Somente **Owner** e **Admin** podem conectar ou desconectar repositórios.
