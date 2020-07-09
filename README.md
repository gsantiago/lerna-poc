# monorepo portabilidade

Este repositório é um monorepo mantido com Lerna que contém três pacotes:

- `portabilidade` - aplicação de portabilidade do squad port
- `existentes` - aplicação de portabilidade do squad existentes
- `common` - responsável por conter código em comum que será compartilhado tanto por `portabilidade` como por `existentes`.

## instalação e preparação

### 1. Clone o repositório e instale suas dependências do Lerna:

`npm install`

### 2. Depois instale as dependências de cada pacote rodando o seguinte comando na raiz do projeto:

`npm run bootstrap`

Este script chama o seguinte script lerna por baixo dos panos: `lerna bootstrap --hoist`. Isso instalará as dependências
de cada pacote na raiz do projeto, fazendo com que eles compartilhem módulos em comum e evitando a duplicação desnecessária de dependências.

## rodar a aplicação

Para rodar portabilidade:

`npx lerna run start --scope=portabilidade`

Para rodar existentes:

`npx lerna run start --scope=existentes`
