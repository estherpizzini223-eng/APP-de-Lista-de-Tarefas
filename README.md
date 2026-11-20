# Aplicativo de Tarefas

Um aplicativo simples de lista de tarefas desenvolvido com HTML, CSS e JavaScript. O projeto permite adicionar, concluir, editar e excluir tarefas, além de acompanhar o progresso por meio de uma barra de progresso e um contador de tarefas concluídas.

## Funcionalidades

- Adicionar novas tarefas.
- Marcar tarefas como concluídas.
- Desmarcar tarefas concluídas.
- Editar tarefas existentes.
- Excluir tarefas.
- Exibir a quantidade de tarefas concluídas e o total de tarefas.
- Atualizar automaticamente a barra de progresso.
- Salvar as tarefas no navegador utilizando `localStorage`.
- Manter as tarefas salvas mesmo após recarregar a página.
- Exibir uma animação de confetes quando todas as tarefas forem concluídas.

## Como executar

1. Baixe ou clone este repositório.
2. Abra a pasta do projeto.
3. Abra o arquivo lista_de_tarefas.html em um navegador.
4. Digite uma tarefa no campo de texto.
5. Clique no botão `+` para adicioná-la.
6. Utilize os ícones de edição e lixeira para modificar ou excluir tarefas.
7. Marque a caixa de seleção para concluir uma tarefa.

Não é necessário instalar dependências para executar a aplicação localmente.

## Tecnologias utilizadas

- **HTML5** — estrutura da aplicação.
- **CSS3** — estilização, organização dos elementos e aparência da interface.
- **JavaScript** — lógica da aplicação, gerenciamento das tarefas e atualização dinâmica da interface.
- **LocalStorage** — armazenamento das tarefas no navegador.
- **tsParticles Confetti** — biblioteca utilizada para criar o efeito de confetes quando todas as tarefas são concluídas.
- **GitHub Pages** — publicação da aplicação na internet.

## Aplicação publicada

A aplicação está disponível no GitHub Pages:



## Principais decisões de implementação

As tarefas são armazenadas em um array de objetos JavaScript. Cada tarefa possui um texto e uma propriedade `completed`, responsável por indicar se ela foi concluída.

A função `addTask()` é responsável por criar novas tarefas e adicioná-las ao array. Depois disso, a função `updateTasksList()` atualiza a lista exibida na página.

A conclusão das tarefas é controlada pela função `toggleTastCompleted()`, que altera o valor de `completed` entre `true` e `false`.

As funções `editTask()` e `deleteTask()` permitem, respectivamente, alterar e remover tarefas da lista.

Foi utilizado o `localStorage` para que as tarefas não sejam perdidas quando a página for recarregada. A função `saveTasks()` transforma o array em JSON e armazena os dados no navegador, enquanto o evento `DOMContentLoaded` recupera essas informações quando a aplicação é aberta novamente.

A barra de progresso é atualizada de acordo com a quantidade de tarefas concluídas em relação ao total de tarefas. O contador também é atualizado automaticamente para mostrar a quantidade de tarefas concluídas.

Por fim, foi utilizada a biblioteca **tsParticles Confetti** para criar o efeito visual de confetes quando todas as tarefas existentes são concluídas.
