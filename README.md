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

Um fluxo simples pode ser representado assim:

```text
Desenvolvedor
      │
      ▼
 git add .
      │
      ▼
git commit -m "feat: adiciona login"
      │
      ▼
git push origin main
      │
      ▼
 GitHub recebe o código
      │
      ▼
 GitHub Actions inicia automaticamente
      │
      ▼
 Compila o projeto
      │
      ▼
 Executa os testes
      │
      ▼
 Verifica se tudo passou
      │
      ▼
 ✅ Tudo certo → Continua
 ❌ Algum erro → Processo interrompido
```

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