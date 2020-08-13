<div align="center">
  <img alt="GoStack"
    src="https://storage.googleapis.com/golden-wind/bootcamp-gostack/header-desafios.png"
  />
</div>

<h2 align="center">
  Desafio 06: Banco de dados e upload de arquivos no Node.js
</h2>

<h3 align="center">
  <img alt="NodeJS"
    src="https://arrayoutofindex.files.wordpress.com/2017/06/node.png" width="180px"/>
</h3>

<p align="center">
  <img alt="language version" src="https://img.shields.io/badge/Node-v_12.14.1-339933?logo=node.js">
  <img alt="language version" src="https://img.shields.io/badge/Yarn-v_1.21.1-2C8EBB?logo=Yarn">
  <img alt="GitHub language count" src="https://img.shields.io/github/languages/count/marllonpontes/gostack-desafio-6">
</p>

<hr/>

<p align="center">
  <a href="#rocket-sobre-o-desafio">Sobre o desafio</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#-funcionalidades">Funcionalidades</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#-tecnologias">Tecnologias</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#-ferramentas">Ferramentas</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#computer-execute-o-projeto">Execute o projeto</a>
</p>

## :rocket: Sobre o desafio

Nesse desafio, você deve continuar desenvolvendo a aplicação de gestão de transações, treinando o que você aprendeu até agora no Node.js junto ao TypeScript, mas dessa vez incluindo o uso de banco de dados com o TypeORM e envio de arquivos com o Multer!

Essa será uma aplicação que deve armazenar transações financeiras de entrada e saída e permitir o cadastro e a listagem dessas transações, além de permitir a criação de novos registros no banco de dados a partir do envio de um arquivo csv.

## 🔥 Funcionalidades

Neste projeto, as rotas foram implementadas usando métodos HTTP:
- **`GET /transactions`**: Essa rota deve retornar uma listagem com todas as transações que você cadastrou até agora, junto com o valor da soma de entradas, retiradas e total de crédito.
- **`POST /transactions`**: A rota deve receber `title`, `value`, `type`, e `category` dentro do corpo da requisição, sendo o `type` o tipo da transação, que deve ser `income` para entradas (depósitos) e `outcome` para saídas (retiradas). Ao cadastrar uma nova transação, ela deve ser armazenada dentro do seu banco de dados, possuindo os campos `id`, `title`, `value`, `type`, `category_id`, `created_at`, `updated_at`.
- **`DELETE /transactions/:id`**: A rota deve deletar uma transação com o `id` presente nos parâmetros da rota;
* **`POST /transactions/import`**: A rota deve permitir a importação de um arquivo com formato `.csv` contendo as mesmas informações necessárias para criação de uma transação `id`, `title`, `value`, `type`, `category_id`, `created_at`, `updated_at`, onde cada linha do arquivo CSV deve ser um novo registro para o banco de dados, e por fim retorne todas as `transactions` que foram importadas para seu banco de dados. O arquivo csv, deve seguir o seguinte [modelo](./src/__tests__/import_template.csv)

## ⚙ Tecnologias

* __NodeJS__
* TypeScript
* Express
* Nodemon
* Yarn
* Jest

## ⛏ Ferramentas

* [Insomnia](https://insomnia.rest/download/)


## :computer: Execute o projeto

Clone este repositório:

```bash
$ git clone https://github.com/marllonpontes/gostack-desafio-6
```

Mova-se para diretório da aplicação:

```bash
$ cd gostack-desafio-6
```

Para instalar as dependências execute:

```bash
yarn install
```

E para iniciar o servidor:

```bash
yarn dev:server
```

<br/>
