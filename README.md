# Projeto de Automação com GitHub Actions - Grupo 5

Este repositório foi desenvolvido para o curso de DevOps ministrado pela APONTI, com o objetivo de demonstrar a automação de processos utilizando o GitHub Actions.

## 👥 Integrantes do Grupo

- [Diego Kauã]
- [Gabriel Der Garabedian]
- [Jhonny Emanoel]
- [Rafael Albuquerque]
- [Nelson Neto]
- [Luiz Felipe]
- [Emanuel Gondim]

---

## 🤖 O que é o GitHub Actions?

<p align="center">
  <img src="https://github.com/user-attachments/assets/e729e7e8-d0f3-487b-aee9-ce40059481a0" alt="GitHub Actions" width="250">
</p>

O **GitHub Actions** é uma ferramenta do próprio GitHub que permite automatizar várias tarefas durante o desenvolvimento de um projeto. Em vez de executar algumas atividades manualmente, como rodar testes ou publicar uma nova versão da aplicação, é possível configurar o GitHub Actions para fazer isso automaticamente sempre que um evento acontecer, como um **push**, a abertura de um **Pull Request** ou a criação de uma **tag**.

Na prática, ele funciona como um "assistente" do projeto. Sempre que uma alteração é enviada para o repositório, o GitHub verifica se existe alguma automação configurada e, caso exista, executa todas as etapas definidas. Isso ajuda a economizar tempo, evitar erros e manter o projeto funcionando corretamente.

---

## 🚀 O que é CI/CD?

Uma das principais utilidades do GitHub Actions é automatizar o processo de **CI/CD**, que significa **Continuous Integration (Integração Contínua)** e **Continuous Delivery/Deployment (Entrega ou Implantação Contínua)**.

### 🔹 Continuous Integration (CI)

A **Integração Contínua** consiste em integrar pequenas alterações ao projeto com frequência. Sempre que um desenvolvedor envia código para o repositório, algumas verificações podem ser executadas automaticamente para garantir que tudo continua funcionando.

Algumas dessas tarefas são:

```text
* ✅ Compilar o projeto;
* ✅ Executar testes automatizados;
* ✅ Verificar a qualidade do código;
* ✅ Procurar possíveis vulnerabilidades;
* ✅ Validar dependências.
```

O objetivo é encontrar erros rapidamente, antes que eles afetem o restante da aplicação.

---

### 🔹 Continuous Delivery / Deployment (CD)

Depois que todas as verificações da CI são aprovadas, entra a etapa de **Continuous Delivery** ou **Continuous Deployment**.

Nessa fase, o sistema pode publicar automaticamente uma nova versão da aplicação ou prepará-la para ser disponibilizada aos usuários.

Isso torna o processo muito mais rápido e reduz bastante a necessidade de tarefas manuais.

---

## ⚙️ Como o GitHub Actions funciona?

O fluxo abaixo representa de forma simplificada como o GitHub Actions executa automaticamente tarefas durante o desenvolvimento.

<p align="center">
  <img src="https://github.com/user-attachments/assets/ae990ec0-e635-49fa-be08-b04348223b00" alt="Fluxo GitHub Actions" width="700">
</p>

<p align="center">
  <em>Figura 1 – Fluxo simplificado do funcionamento do GitHub Actions.</em>
</p>

## Após um git push, o GitHub identifica que existe um workflow configurado e inicia automaticamente todas as etapas necessárias.

## 💻 Exemplo Prático

Imagine uma equipe desenvolvendo uma API em **Java + Spring Boot**.

Depois de terminar uma nova funcionalidade, um dos desenvolvedores executa:

```bash
git add .
git commit -m "feat: adiciona autenticação JWT"
git push origin feature/login
```

Assim que o **git push** é enviado, o GitHub Actions pode iniciar automaticamente uma série de verificações.

Entre elas:

- Compilar o projeto;
- Executar os testes;
- Verificar a qualidade do código.

Se algum teste falhar, o desenvolvedor recebe essa informação e pode corrigir o problema antes que o código seja integrado ao projeto principal.

---

---

## 📊 Comparação entre o processo manual e automatizado

A tabela abaixo mostra como o GitHub Actions simplifica diversas etapas do desenvolvimento de software quando comparado ao processo realizado manualmente.

| **Processo**          | **Sem GitHub Actions** | **Com GitHub Actions** |
| :-------------------- | :--------------------- | :--------------------- |
| Execução dos testes   | Manual                 | Automática             |
| Verificação do código | Manual                 | Automática             |
| Deploy da aplicação   | Manual                 | Automatizado           |
| Tempo de entrega      | Maior                  | Menor                  |
| Chance de erro        | Alta                   | Reduzida               |

> **Observação:** Ao automatizar essas etapas, o GitHub Actions torna o desenvolvimento mais ágil, confiável e padronizado, permitindo que a equipe foque no desenvolvimento de novas funcionalidades em vez de tarefas repetitivas.

---

## 🌍 Alguns exemplos de uso

Hoje em dia muitas empresas utilizam o GitHub Actions para automatizar tarefas como:

- 🚀 Fazer deploy de aplicações;
- 🧪 Executar testes automaticamente;
- 🔍 Verificar a qualidade do código;
- 📦 Criar novas versões do sistema;
- 📚 Gerar documentação;
- 📢 Enviar notificações quando algum processo falha.

---

## Benefícios do GitHub Actions

O GitHub Actions oferece diversas vantagens para equipes de desenvolvimento, principalmente por automatizar tarefas repetitivas e reduzir erros durante o desenvolvimento.

### Principais benefícios

- **Automação de tarefas:** elimina a necessidade de executar manualmente processos como testes, compilação e deploy.

- **Maior qualidade do código:** executa testes automaticamente sempre que uma alteração é enviada ao repositório, ajudando a identificar problemas rapidamente.

- **Mais produtividade:** os desenvolvedores podem focar na implementação de novas funcionalidades enquanto tarefas repetitivas são executadas automaticamente.

- **Melhor colaboração:** como todas as alterações passam pelas mesmas validações, o trabalho em equipe se torna mais organizado e confiável.

- **Entrega mais rápida:** automatiza o processo de integração e entrega da aplicação, reduzindo o tempo entre o desenvolvimento e a publicação.

- **Feedback imediato:** caso algum teste ou validação falhe, o GitHub informa rapidamente o erro, facilitando a correção.

- **Integração nativa com o GitHub:** não é necessário utilizar ferramentas externas para criar pipelines de automação.

- **Suporte a diversas tecnologias:** funciona com diferentes linguagens de programação e frameworks, como Java, Python, JavaScript, C#, PHP, Go, entre outros.

---

## 🚀 Funcionalidades do Workflow

Depois que o GitHub Actions é configurado, o **workflow** passa a ser responsável por executar automaticamente as tarefas definidas para o projeto. Podemos imaginá-lo como um roteiro de execução: em vez de uma pessoa precisar lembrar e realizar cada etapa manualmente, o GitHub segue uma sequência de instruções previamente organizada pelos desenvolvedores.

Esse processo sempre começa quando acontece um **evento de gatilho** (_trigger_). Um evento nada mais é do que uma ação realizada dentro do repositório que informa ao GitHub que chegou o momento de iniciar a automação. Entre os exemplos mais comuns estão o envio de código (_push_), a abertura de um _Pull Request_ ou a criação de uma nova versão do projeto.

<p align="center">
  <img src="https://github.com/user-attachments/assets/aea1ef17-fc88-4821-b68b-6d58073670e2" alt="Fluxograma de um Workflow" width="700" >
</p>

<p align="center">
  <em>Figura 2 – Organização de um workflow no GitHub Actions.</em>
</p>

A imagem acima ilustra esse funcionamento. Observe que o processo acontece de cima para baixo. Primeiro ocorre o **evento de gatilho**, representado pelo envio de código (_push_). Em seguida, o GitHub localiza o **workflow**, que é um arquivo escrito em **YAML** onde os desenvolvedores descrevem todas as tarefas que deverão ser executadas e a ordem em que elas acontecerão.

Depois disso entram em ação os **jobs**. Podemos imaginar cada job como um **bloco de trabalho**, responsável por uma parte específica da automação. Em vez de concentrar todas as tarefas em um único lugar, o workflow pode ser dividido em diferentes jobs para deixar o processo mais organizado e facilitar sua manutenção.

Cada **job** é dividido em várias **steps** (etapas), que funcionam como pequenas instruções executadas em sequência. Observe como isso acontece na imagem:

```text
Workflow
   │
   ├── Job 1
   │     ├── 📥 Baixar o código
   │     ├── 📦 Instalar dependências
   │     └── 🧪 Executar testes
   │
   └── Job 2
         ├── 🏗️ Build
         └── 🚀 Deploy
```

Perceba que cada **job** possui uma responsabilidade diferente. O primeiro prepara e verifica o projeto, enquanto o segundo constrói a aplicação (_build_) e, quando configurado, realiza sua publicação (_deploy_). Assim, o workflow fica organizado em blocos de trabalho menores, tornando o processo mais fácil de entender, manter e expandir conforme o projeto evolui.

É importante destacar que essa organização pode variar de acordo com o projeto. Alguns workflows possuem apenas um job com poucas etapas, enquanto outros são divididos em vários blocos de trabalho para automatizar processos mais complexos.

Embora cada projeto tenha necessidades diferentes, algumas tarefas aparecem com frequência na maioria dos workflows, como:

| Etapa                        | Finalidade                                                                 |
| :--------------------------- | :------------------------------------------------------------------------- |
| 📥 **Baixar o código**       | Obtém a versão mais recente do projeto para iniciar a execução.            |
| 📦 **Instalar dependências** | Prepara o ambiente com tudo o que a aplicação precisa para funcionar.      |
| 🧪 **Executar testes**       | Verifica se as funcionalidades continuam funcionando corretamente.         |
| 🔍 **Analisar o código**     | Confere se o projeto segue os padrões definidos pela equipe.               |
| 🚀 **Publicar a aplicação**  | Disponibiliza uma nova versão do sistema, quando essa etapa é configurada. |

Assim como acontece ao seguir uma receita de bolo, não faz sentido decorar o bolo antes de assá-lo. Da mesma forma, um workflow executa suas etapas em ordem, garantindo que cada uma seja concluída antes da próxima começar.

Em resumo, um workflow funciona como um roteiro automatizado que orienta o GitHub sobre quais tarefas devem ser executadas e em qual ordem. Essa padronização reduz o trabalho manual, aumenta a confiabilidade das verificações e contribui para um processo de desenvolvimento mais organizado, seguro e eficiente. Além de permitir que os desenvolvedores concentrem seus esforços na evolução do software, e não na execução de tarefas repetitivas.

## 🛠️ Como rodar o projeto localmente

_(integrante 4)_

## 🧪 Estrutura dos Testes

A execução dos testes em um evento do GitHub Actions ocorre de forma isolada e automatizada a partir de um runner (um container, geralmente Linux Ubuntu) na nuvem. Sempre que ocorre um evento, como o **push** ou **pull request**, por exemplo, o GitHub cria um ambiente novo e executa a pipeline de testes definida no arquivo _YAML_. A seguir, um exemplo de arquivo _YAML_ para executar testes em Node.js nos eventos de push ou pull request.

```yaml
name: Testes Automatizados

on:
  push:
    branches: [main]
  pull_request:
    branches: [main]

jobs:
  teste-exemplo:
    runs-on: ubuntu-latest

    steps:
      - name: Baixar Código do Repositório
        uses: actions/checkout@v4

      - name: Configurar Node.js
        uses: actions/setup-node@v4
        with:
          node-version: "20"

      - name: Instalar Dependências
        run: npm ci

      - name: Executar Testes
        run: npm test
```

Quando um **push** passa com sucesso nos testes, o workflow é finalizado com o status <span style="color:#1a7f37;">verde de sucesso</span>, ou seja, as validações automáticas foram validadas e o código está pronto para o próximo passo do ciclo da entrega. Quando um push falha nos testes, o workflow é marcado com o status de <span style="color:#d1242f;">falha vermelho</span>, o código é aceito no repositório, mas as verificações de status são reprovadas, emitindo notificações sobre essas falhas (geralmente por email). Caso exista uma proteção de branch principal configurada (main ou master), a integração do push ao repositório é bloqueada.

<p align=center style="margin-top:3em;">
  <img src="https://i.ibb.co/tM0tfT0C/teste-passou.png" alt="Testes passaram"></p>
<p align="center" style="margin-top:-1em;font-style:italic;">Testes passaram com sucesso.</p>

<p align=center style="margin-top:3em;">
  <img src="https://i.ibb.co/KzDVYSGT/teste-erro.png" alt="Testes falharam">
</p>
<p align="center" style="margin-top:-1em;margin-bottom:2em;font-style:italic;">Testes falharam.</p>

Quando os testes falham dentro de um **pull request**, ele ganha uma sinalização vermelha explícita, alertando a equipe a impedir que o código com erro seja integrado ao projeto. O GitHub exibe um _X_ vermelho ao lado do nome do teste que falhou, junto com o botão _Details_ que leva direto para a linha de log onde o erro aconteceu. Caso exista uma proteção de branch ativa, o botão _Merge Pull Request_ fica cinza e bloqueado, impedindo que qualquer desenvolvedor envie bug para a branch principal.

<p align=center style="margin-top:3em;">
  <img src="https://i.ibb.co/tPbKqwfp/pull-request-erro.png" alt="Testes falharam no PR">
</p>
<p align="center" style="margin-top:-1em;margin-bottom:2em;font-style:italic;">Testes falharam no Pull Request.</p>

## 💻 Tecnologias Utilizadas

Nos últimos anos, houve uma grande mudança na estratégia das empresas de tecnologia. Na década passada, era comum o mercado adotar ferramentas isoladas para resolver problemas específicos. Hoje, a tendência é a criação de ecossistemas integrados que centralizam processos. Isso reduz a complexidade de gerenciar inúmeras credenciais e simplifica a análise de logs, eliminando a necessidade de lidar com múltiplas plataformas.

O GitHub reflete exatamente essa evolução: o que antes era apenas um repositório de código, hoje se consolidou como uma plataforma de desenvolvimento completa (Developer Platform) graças à integração de diversas tecnologias. Abaixo estão listadas as principais tecnologias que sustentam o funcionamento do GitHub Actions.

### 1. YAML (`.yml` ou `.yaml`)
 
É a linguagem de serialização de dados usada para escrever os arquivos de configuração dos workflows (fluxos de trabalho). Todos os comandos, horários e passos que o GitHub Actions deve seguir são descritos em arquivos YAML dentro da pasta `.github/workflows/`.
 
- **Para que serve:** é uma linguagem limpa, legível por humanos, baseada em indentação (espaçamentos), o que evita a complexidade de códigos cheios de chaves ou colchetes.

### 2. Containers e Docker
 
O GitHub Actions é totalmente baseado em isolamento de ambiente. Quando o seu fluxo começa a rodar, ele inicia uma máquina virtual limpa ou um container Docker.
 
- **Para que serve:** garante que os seus testes rodem em um ambiente idêntico todas as vezes, sem "vôos cegos" ou o famoso "na minha máquina funciona". Você pode rodar seus fluxos em containers de Node.js, Python, Ubuntu, etc.

### 3. Ambientes de Execução (Runners)
 
<p align=center style="margin-top:1em;margin-bottom:1em;">
  <img src="https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black" alt="Linux">
  <img src="https://img.shields.io/badge/Windows_Server-0078D6?style=for-the-badge&logo=windows&logoColor=white" alt="Windows Server">
  <img src="https://img.shields.io/badge/macOS-000000?style=for-the-badge&logo=apple&logoColor=white" alt="macOS">
</p>
Os Runners são as máquinas que realmente executam o código dos seus fluxos de automação. O GitHub Actions utiliza tecnologias de sistemas operacionais nativos para disponibilizar essas máquinas em nuvem:
 
- **Linux (Ubuntu)** — o mais comum, rápido e leve.
- **Windows Server** — para projetos que dependem do ecossistema .NET legado ou ferramentas específicas da Microsoft.
- **macOS** — fundamental para quem compila aplicativos iOS (Swift/Objective-C) ou utilitários para Mac.

### 4. JavaScript / TypeScript (Node.js)
 
<p align=center style="margin-top:1em;margin-bottom:1em;">
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="JavaScript">
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript">
  <img src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=node.js&logoColor=white" alt="Node.js">
</p>
Se você for criar uma Action personalizada para disponibilizar no Marketplace do GitHub, a tecnologia padrão recomendada para desenvolvimento dessas extensões é o Node.js (JavaScript/TypeScript). O GitHub fornece kits de desenvolvimento (SDKs) oficiais focados em Node.js para interagir com as APIs deles.

## 📝 Conclusão

O GitHub Actions representa uma evolução significativa na forma como equipes de desenvolvimento organizam e automatizam seus processos. Ao longo deste projeto, exploramos como essa ferramenta permite configurar pipelines de CI/CD diretamente no repositório, eliminando a dependência de plataformas externas e simplificando o fluxo de trabalho.

Vimos que, por meio de workflows escritos em YAML, é possível automatizar desde a execução de testes até o deploy da aplicação, garantindo que cada alteração enviada ao repositório passe por verificações automáticas antes de ser integrada ao projeto principal. Isso reduz erros, aumenta a confiabilidade do código e permite que os desenvolvedores foquem no que realmente importa: construir novas funcionalidades.

Além disso, a organização em jobs e steps torna os workflows flexíveis e escaláveis, adaptando-se tanto a projetos simples quanto a pipelines mais complexas.

Em suma, o GitHub Actions não é apenas uma ferramenta de automação — é uma mudança de mentalidade no desenvolvimento de software moderno, tornando o processo mais ágil, seguro e colaborativo.

Automatize, teste, entregue — tudo dentro do GitHub. 🚀
