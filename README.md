# APONTI-FAP-GRUPO5
 
<!-- ========================= INÍCIO DA SEÇÃO 3 - JHONNY ========================= -->

## ⚙️ Funcionalidades de um Workflow

Depois que o GitHub Actions é configurado, o **workflow** passa a ser responsável por executar automaticamente as tarefas definidas para o projeto. Podemos imaginá-lo como um roteiro de execução: em vez de uma pessoa precisar lembrar e realizar cada etapa manualmente, o GitHub segue uma sequência de instruções previamente organizada pelos desenvolvedores.

Esse processo sempre começa quando acontece um **evento de gatilho** (*trigger*). Um evento nada mais é do que uma ação realizada dentro do repositório que informa ao GitHub que chegou o momento de iniciar a automação. Entre os exemplos mais comuns estão o envio de código (*push*), a abertura de um *Pull Request* ou a criação de uma nova versão do projeto.

<p align="center">
  <img src="assets/fluxograma-workflow.png" alt="Fluxograma representando o funcionamento de um workflow no GitHub Actions" width="850">
</p>

A imagem acima ilustra esse funcionamento. Observe que o processo acontece de cima para baixo. Primeiro ocorre o **evento de gatilho**, representado pelo envio de código (*push*). Em seguida, o GitHub localiza o **workflow**, que é um arquivo escrito em **YAML** onde os desenvolvedores descrevem todas as tarefas que deverão ser executadas e a ordem em que elas acontecerão.

Depois disso entram em ação os **jobs**. Podemos imaginar cada job como um **bloco de trabalho**, responsável por uma parte específica da automação. Em vez de concentrar todas as tarefas em um único lugar, o workflow pode ser dividido em diferentes jobs para deixar o processo mais organizado e facilitar sua manutenção.

Cada job é formado por várias **steps** (etapas), que funcionam como pequenas instruções executadas em sequência. Na imagem, por exemplo, o primeiro job reúne as etapas de preparação e validação do projeto, como baixar o código, instalar as dependências e executar os testes. Já o segundo job é responsável pela construção (*build*) e publicação (*deploy*) da aplicação.

É importante destacar que essa organização pode variar de acordo com o projeto. Alguns workflows possuem apenas um job com poucas etapas, enquanto outros são divididos em vários blocos de trabalho para automatizar processos mais complexos.

Entre as tarefas mais comuns que um workflow pode executar estão:

| Etapa                        | Finalidade                                                                 |
| :--------------------------- | :------------------------------------------------------------------------- |
| 📥 **Baixar o código**       | Obtém a versão mais recente do projeto para iniciar a execução.            |
| 📦 **Instalar dependências** | Prepara o ambiente com tudo o que a aplicação precisa para funcionar.      |
| 🧪 **Executar testes**       | Verifica se as funcionalidades continuam funcionando corretamente.         |
| 🔍 **Analisar o código**     | Confere se o projeto segue os padrões definidos pela equipe.               |
| 🚀 **Publicar a aplicação**  | Disponibiliza uma nova versão do sistema, quando essa etapa é configurada. |

Assim como acontece ao seguir uma receita, cada etapa depende da conclusão da anterior para que o processo continue corretamente. Se uma delas encontrar um problema, o GitHub interrompe a execução e informa exatamente onde ocorreu a falha. Dessa forma, a equipe consegue identificar e corrigir erros rapidamente, antes que eles avancem para as próximas fases do desenvolvimento.

Em resumo, um workflow funciona como um roteiro automatizado que orienta o GitHub sobre quais tarefas devem ser executadas e em qual ordem. Essa padronização reduz o trabalho manual, aumenta a confiabilidade das verificações e contribui para um processo de desenvolvimento mais organizado, seguro e eficiente.

<!-- ========================== FIM DA SEÇÃO 3 - JHONNY ========================== -->