![Wallpaper GoStack](https://user-images.githubusercontent.com/58411170/79023960-f326d100-7b57-11ea-9a3b-d3fd0d6bf6bd.png)

<h2 align="center">
  Desafio 02: Conceitos do NodeJS
</h2> 
 
<p align="center">
  Criado durante o bootcamp GoStack 11.
</p>
 
<p align="center">
 
  <img alt="GitHub language count" src="https://img.shields.io/github/languages/count/gabriel-antero/desafio-conceitos-node">
  <img alt="GitHub top language" src="https://img.shields.io/github/languages/top/gabriel-antero/desafio-conceitos-node"> 
  <img alt="GitHub repo size" src="https://img.shields.io/github/repo-size/gabriel-antero/desafio-conceitos-node">
  <img alt="GitHub last commit" src="https://img.shields.io/github/last-commit/gabriel-antero/desafio-conceitos-node">
  
</p>

<p align="center">
  <a href="https://github.com/gabriel-antero/desafio-conceitos-node#information_source-sobre-o-desafio">Sobre o desafio<a/> |
  <a href="https://github.com/gabriel-antero/desafio-conceitos-node#dart-objetivos-a-realizar">Objetivos a realizar<a/> |
  <a href="https://github.com/gabriel-antero/desafio-conceitos-node#memo-licen%C3%A7a">LICENÇA<a/>
</p>
 
## :information_source: Sobre o desafio

Aplicação para armazenar repositórios do seu portfólio, que irá permitir a criação, listagem, atualização e remoção 
dos repositórios, e além disso permitir que os repositórios possam receber "likes".

Feito utilizando testes automatizados.

## :dart: Objetivos a realizar
  Criar os comandos das rotas e realizar os testes fornecidos, conforme os criterios a seguir:
  
<h3 align="center">Rotas da aplicação</h3>

- [X] **`POST /repositories`**: A rota deve receber `title`, `url` e `techs` dentro do corpo da requisição, sendo a URL o link para o github desse repositório. Ao cadastrar um novo projeto, ele deve ser armazenado dentro de um objeto no seguinte formato: `{ id: "uuid", title: 'Desafio Node.js', url: 'http://github.com/...', techs: ["Node.js", "..."], likes: 0 }`; Certifique-se que o ID seja um UUID, e de sempre iniciar os likes como 0.

- [X] **`GET /repositories`**: Rota que lista todos os repositórios;

- [X] **`PUT /repositories/:id`**: A rota deve alterar apenas o `title`, a `url` e as `techs` do repositório que possua o `id` igual ao `id` presente nos parâmetros da rota;

- [X] **`DELETE /repositories/:id`**: A rota deve deletar o repositório com o `id` presente nos parâmetros da rota;

- [X] **`POST /repositories/:id/like`**: A rota deve aumentar o número de likes do repositório específico escolhido através do `id` presente nos parâmetros da rota, a cada chamada dessa rota, o número de likes deve ser aumentado em 1;

<h3 align="center">Específicação dos testes</h3>
<p align="center">Necessário realizar os seguintes testes:

- [X] **`should be able to create a new repository`**: Para que esse teste passe, sua aplicação deve permitir que um repositório seja criado, e retorne um json com o projeto criado.

- [X] **`should be able to list the repositories`**: Para que esse teste passe, sua aplicação deve permitir que seja retornado um array com todos os repositórios que foram criados até o momento.

- [X] **`should be able to update repository`**: Para que esse teste passe, sua aplicação deve permitir que sejam alterados apenas os campos `url`, `title` e `techs`.

- [X] **`should not be able to update a repository that does not exist`**: Para que esse teste passe, você deve validar na sua rota de update se o id do repositório enviado pela url existe ou não. Caso não exista, retornar um erro com status `400`.

- [X] **`should not be able to update repository likes manually`**: Para que esse teste passe, você não deve permitir que sua rota de update altere diretamente os likes desse repositório, mantendo o mesmo número de likes que o repositório já possuia antes da atualização. Isso porque o único lugar que deve atualizar essa informação é a rota de responsável por aumentar o número de likes.

- [X] **`should be able to delete the repository`**: Para que esse teste passe, você deve permitir que a sua rota de delete exclua um projeto, e ao fazer a exclusão, ele retorne uma resposta vazia, com status `204`.

- [X] **`should not be able to delete a repository that does not exist`**: Para que esse teste passe, você deve validar na sua rota de delete se o id do repositório enviado pela url existe ou não. Caso não exista, retornar um erro com status `400`.

- [X] **`should be able to give a like to the repository`**: Para que esse teste passe, sua aplicação deve permitir que um repositório com o id informado possa receber likes. O valor de likes deve ser incrementado em 1 a cada requisição, e como resultado, retornar um json contendo o repositório com o número de likes atualizado.

- [X] **`should not be able to like a repository that does not exist`**: Para que esse teste passe, você deve validar na sua rota de like se o id do repositório enviado pela url existe ou não. Caso não exista, retornar um erro com status `400`.

## :memo: LICENÇA

Projeto sobre licença MIT. Mais informações em [LICENÇA](https://github.com/gabriel-antero/desafio-conceitos-node/blob/master/LICENSE).

---

Trechos desse conteúdo copiado do arquivo do desafio.
