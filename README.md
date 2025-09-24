# 📊 banco-api-performance

## 📌 Introdução
Este repositório contém testes de performance desenvolvidos em **JavaScript** utilizando a ferramenta **k6**.  
O objetivo é validar o desempenho e a resiliência da API de um sistema bancário, simulando diferentes cenários de carga e usuários concorrentes.

---

## 🛠 Tecnologias utilizadas
- [Node.js](https://nodejs.org/) – Gerenciamento de dependências e execução de scripts.
- [k6](https://k6.io/) – Ferramenta para execução dos testes de performance.
- [JavaScript](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript) – Linguagem utilizada para escrever os testes.

---

## 📂 Estrutura do repositório
```
banco-api-performance/
├── fixtures/              # Dado de entrada para os testes (ex: usuários, payload)
│   └── postLogin.json
├── helpers/               # Funções utilitárias reutilizaveis para interação com a API
│   └── autenticacao.js
├── tests/                 # Contém os arquivos de teste organizados por funcionalidade
│   ├── login.test.js      # Testes relacionados à autenticação
│   ├── transferencias.test.js # Testes relacionados a transferências bancárias
├── config/                 # Arquivo de configuração de variáveis de ambiente
│   └── variaveis.js
├── utils/                 # Funções auxiliares para reaproveitamento de código
│   └── variaveis.js
└── README.md              # Documentação do projeto
```

---

## 🎯 Objetivo de cada grupo de arquivos
- **fixtures/** → Dado de entrada para os testes (ex: usuários, payload) 
- **helpers/** → Funções utilitárias reutilizaveis para interação com a API. 
- **tests/** → Contém os arquivos de teste organizados por funcionalidade. 
- **config/** → Arquivo de configuração de variáveis de ambiente   
- **utils/** → Funções auxiliares para reaproveitamento de código  

---

## ⚙️ Modo de instalação
1. Clone o repositório:
   ```bash
   git clone https://github.com/Alihito2127/banco-api-performance.git
   cd banco-api-performance
   ```

2. Instale as dependências:
   ```bash
   npm install
   ```

3. Certifique-se de ter o **k6** instalado globalmente:  
   [Guia de instalação oficial](https://grafana.com/docs/k6/latest/get-started/installation/)

---

## 🚀 Modo de execução do projeto
1. Defina a variável de ambiente **BASE_URL**, apontando para a URL base da sua API:  
   - Linux/Mac:
     ```bash
     export BASE_URL=http://localhost:3000
     ```
   - Windows (PowerShell):
     ```powershell
     $env:BASE_URL="http://localhost:3000"
     ```

2. Execute um teste, por exemplo:
   ```bash
   k6 run tests/login.test.js
   ```

---

## 📈 Relatórios e monitoramento em tempo real
O **k6** permite acompanhar a execução com um **dashboard web em tempo real** e exportar relatórios para arquivo HTML.

Exemplo de execução:
```powershell
$env:K6_WEB_DASHBOARD="true"
$env:K6_WEB_DASHBOARD_EXPORT="$PWD\resultado.html"
k6 run tests\login.test.js
```

- `K6_WEB_DASHBOARD=true` → Habilita o acompanhamento em tempo real via navegador.  
- `K6_WEB_DASHBOARD_EXPORT=resultado.html` → Exporta o relatório final em HTML.  
- `BASE_URL=http://localhost:3000` → Define a URL base da API sendo testada.  

Após a execução, basta abrir o arquivo **resultado.html** no navegador para visualizar o relatório completo.

---

👉 Repositório oficial: [banco-api-performance](https://github.com/Alihito2127/banco-api-performance)  
