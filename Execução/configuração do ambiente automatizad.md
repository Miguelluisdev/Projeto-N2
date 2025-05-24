# 🤖 Automação de Testes - QAZANDO Shop E-Commerce

## 🚀 Stack Tecnológica

| Ferramenta   | Descrição                                                        |
|---------------|------------------------------------------------------------------|
| **CodeceptJS**  | Framework de automação de testes end-to-end.                      |
| **Playwright**  | Biblioteca para controle de navegador e execução de testes.       |
| **Git**         | Controle de versão e colaboração.                                 |
| **Faker.js**    | Geração de dados falsos para testes dinâmicos.                   |
| **Page Object Model** | Padrão de projeto para organização e manutenção dos testes.     |
| **JavaScript**  | Linguagem base para os testes.                                    |

---

## 🏗️ Estrutura do Projeto

```

📦 tests/
├── 📁 pages/              # Objetos de página (Page Objects)
├── 📁 steps/              # Arquivos de passos (passos de teste reutilizáveis)
├── 📁 output/             # Relatórios e evidências de teste
├── 📜 test.js             # Arquivo de exemplo de teste
└── 📜 config.js           # Configuração do CodeceptJS
📦 .gitignore
📦 package.json
📦 README.md

````

---

## ⚙️ Pré-Requisitos

- [Node.js (v18+)](https://nodejs.org/)
- [Git](https://git-scm.com/)

---

## 🔧 Instalação

1️⃣ Clone o repositório:

```bash
git clone https://github.com/seu-usuario/qazando-shop-automation.git
cd qazando-shop-automation
````

2️⃣ Instale as dependências:

```bash
npm install
```

---

## ⚙️ Configuração do CodeceptJS

O arquivo `codecept.conf.js` (ou `config.js`) contém:

```js
const { setHeadlessWhen } = require('@codeceptjs/configure');
setHeadlessWhen(process.env.HEADLESS);

exports.config = {
  tests: './tests/*.js',
  output: './tests/output',
  helpers: {
    Playwright: {
      url: 'https://qazando-shop.com', // URL base
      show: true,                      // Mostrar navegador 
      browser: 'chromium'
    }
  },
  include: {
    I: './steps_file.js',
    homePage: './tests/pages/homePage.js',
    productPage: './tests/pages/productPage.js',
    checkoutPage: './tests/pages/checkoutPage.js'
  },
  bootstrap: null,
  mocha: {},
  name: 'qazando-shop-automation'
}
```

---

## 🧪 Execução dos Testes

* Rodar todos os testes:

```bash
npx codeceptjs run --plugins allure
```

* Rodar com navegador visível (útil para aprendizado):

```bash
npx codeceptjs run --debug
```

* Rodar um teste específico:

```bash
npx codeceptjs run tests/test.js
```

---

## 🎨 Uso do Page Object Model

Cada página tem um arquivo correspondente dentro da pasta `tests/pages/`. Exemplo:

```js
// homePage.js
const { I } = inject();

module.exports = {
  fields: {
    searchInput: 'input[placeholder="Pesquisar..."]'
  },
  searchProduct(product) {
    I.fillField(this.fields.searchInput, product);
    I.pressKey('Enter');
  }
};
```

---

## 🎲 Geração de Dados Dinâmicos com Faker.js

Arquivo `utils/fakerGenerator.js`:

```js
const { faker } = require('@faker-js/faker');

module.exports = {
  generateUser() {
    return {
      name: faker.person.fullName(),
      email: faker.internet.email(),
      password: faker.internet.password()
    }
  }
};
```

Exemplo de uso em teste:

```js
const faker = require('../utils/fakerGenerator');

Scenario('Cadastro de usuário dinâmico', ({ I }) => {
  const user = faker.generateUser();
  I.fillField('Nome', user.name);
  I.fillField('Email', user.email);
  I.fillField('Senha', user.password);
  I.click('Cadastrar');
});
```

---

## 📚 Aprendizado e Evolução

* Estudar padrões de **Page Object Model** para organizar os testes.
* Integrar o **Allure** ou outra ferramenta de relatórios para melhores insights.
* Praticar testes em múltiplos navegadores (Chromium, Firefox, Webkit).
* Realizar integração contínua com GitHub Actions ou outra ferramenta de CI/CD.

---

## 🏁 Conclusão

Este repositório serve como **base para aprendizado e prática de automação de testes** em e-commerce utilizando CodeceptJS e Playwright. Sinta-se à vontade para evoluir o projeto, adicionar novos cenários e aplicar melhores práticas de testes automatizados. vá para https://github.com/Miguelluisdev/Projeto-N2/tree/main/Execu%C3%A7%C3%A3o/Automa%C3%A7%C3%A3o%20dos%20testes ver os codigos

