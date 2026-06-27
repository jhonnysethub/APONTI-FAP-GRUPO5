# APONTI-FAP-GRUPO5
GitHub Actions e automação de processos

## 🤖 O que é o GitHub Actions?

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

Após um git push, o GitHub identifica que existe um workflow configurado e inicia automaticamente todas as etapas necessárias.
---
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

* Compilar o projeto;
* Executar os testes;
* Verificar a qualidade do código.

Se algum teste falhar, o desenvolvedor recebe essa informação e pode corrigir o problema antes que o código seja integrado ao projeto principal.

---

## 🌍 Alguns exemplos de uso

Hoje em dia muitas empresas utilizam o GitHub Actions para automatizar tarefas como:

* 🚀 Fazer deploy de aplicações;
* 🧪 Executar testes automaticamente;
* 🔍 Verificar a qualidade do código;
* 📦 Criar novas versões do sistema;
* 📚 Gerar documentação;
* 📢 Enviar notificações quando algum processo falha.

---

## Benefícios do GitHub Actions

O GitHub Actions oferece diversas vantagens para equipes de desenvolvimento, principalmente por automatizar tarefas repetitivas e reduzir erros durante o desenvolvimento.

### Principais benefícios

- **Automação de tarefas:** elimina a necessidade de executar manualmente processos como testes, compilação e deploy.

- **Maior qualidade do código:** executa testes automaticamente sempre que uma alteração é enviada ao repositório, ajudando a identificar problemas rapidamente.

- **Mais produtividade:** os desenvolvedores podem focar na implementação de novas funcionalidades enquanto tarefas repetitivas são executadas automaticamente.

- **Melhor colaboração:** como todas as alterações passam pelas mesmas validações, o trabalho em equipe se torna mais organizado e confiável.

-  **Entrega mais rápida:** automatiza o processo de integração e entrega da aplicação, reduzindo o tempo entre o desenvolvimento e a publicação.

- **Feedback imediato:** caso algum teste ou validação falhe, o GitHub informa rapidamente o erro, facilitando a correção.

- **Integração nativa com o GitHub:** não é necessário utilizar ferramentas externas para criar pipelines de automação.

- **Suporte a diversas tecnologias:** funciona com diferentes linguagens de programação e frameworks, como Java, Python, JavaScript, C#, PHP, Go, entre outros.

---