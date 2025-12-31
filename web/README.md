# 🧪 Testes Automatizados – Webdojo (Cypress)

Este projeto contém a automação de testes end-to-end da aplicação **Webdojo**, utilizando **Cypress** para garantir qualidade, estabilidade e confiança nas funcionalidades Web.

---

## ✅ Tecnologias Utilizadas
- Cypress
- Node.js
- JavaScript
- npm
- Serve (para subir a aplicação Webdojo localmente)

---

## 📁 Estrutura do Projeto

A automação segue a organização abaixo:

```
cypress
 ├── e2e
 │    └── *.cy.js            # Arquivos de testes E2E
 │
 ├── fixtures
 │    ├── cep.json           # Massa de dados de CEP
 │    ├── consultancy.json   # Massa de dados do fluxo de consultoria
 │    └── document.pdf       # Arquivo utilizado em testes de upload
 │
 ├── support
 │    ├── actions
 │    │    └── consultancy.actions.js   # Ações reutilizáveis
 │    ├── commands.js        # Comandos customizados do Cypress
 │    ├── e2e.js             # Configurações globais
 │    └── utils.js           # Funções utilitárias
```

---

## ▶️ Executando a Aplicação Webdojo

A aplicação Webdojo está no mesmo repositório dos testes.

Antes de rodar os testes, inicie a aplicação:

```bash
npm run dev
```

A aplicação será servida na porta **3000**.

---

## 🧾 Scripts Disponíveis

Os seguintes scripts estão configurados no `package.json`:

```json
"scripts": {
  "dev": "serve -s dist -p 3000",
  "test": "npx cypress run --config viewportWidth=1440,viewportHeight=900",
  "test:ui": "npx cypress open",
  "test:login": "npx cypress run --spec cypress/e2e/login.cy.js --config viewportWidth=1440,viewportHeight=900",
  "test:login:mobile": "npx cypress run --spec cypress/e2e/login.cy.js --config viewportWidth=414,viewportHeight=896"
}
```

---

## 🚀 Como Executar os Testes

### 1️⃣ Instalar dependências
```bash
npm install
```

### 2️⃣ Subir a aplicação
```bash
npm run dev
```

### 3️⃣ Executar os testes

#### 🔵 Modo interativo (Cypress UI)
```bash
npm run test:ui
```

#### 🟢 Rodar todos os testes em modo headless
```bash
npm run test
```

#### 🔐 Rodar apenas testes de login (Desktop)
```bash
npm run test:login
```

#### 📱 Rodar testes de login em resolução Mobile
```bash
npm run test:login:mobile
```

---

## 🧩 Fixtures

A pasta `fixtures` contém arquivos de massa de dados e arquivos utilizados nos testes:

- `cep.json` – dados de CEP  
- `consultancy.json` – massa de dados do fluxo de consultoria  
- `document.pdf` – documento para upload  

---

## 🛠️ Support e Ações

### `support/commands.js`
Contém comandos customizados do Cypress reutilizáveis ao longo do projeto.

### `support/actions`
Contém ações encapsuladas responsáveis por interações com a aplicação, promovendo reutilização e manutenção do código.

---

## 🎯 Objetivo do Projeto

Garantir confiabilidade e segurança nas funcionalidades da plataforma Webdojo através de testes automatizados consistentes, permitindo:

- Validação de fluxos críticos  
- Regressão automatizada  
- Maior qualidade nas entregas  

---

## 🧑‍💻 Autor
Projeto mantido por **Carlos Henrique – QA Engineer**.
