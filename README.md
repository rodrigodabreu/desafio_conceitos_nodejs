<img alt="GoStack" src="https://storage.googleapis.com/golden-wind/bootcamp-gostack/header-desafios.png" />

<h3 align="center">
  Desafio 02: Conceitos do Node.js
</h3>

<p align="center">“Não espere para plantar, apenas tenha paciência para colher”!</blockquote>


## :rocket: Sobre o desafio

Nesse desafio foi solicitado a criação uma aplicação Node.js para treinar os conhecimentos adquiridos ao longo das aulas do nível 01.

A aplicação tem como objetivo armazenar repositórios de um portfólio, que irá permitir a criação, listagem, atualização e remoção dos repositórios, e além disso permitir que os repositórios possam receber "likes".

### Template da aplicação

O template da aplicaço já foi fornecido pela :rocket Rockeseat com o intuito de gerar mais agilidade no processo de correção dos desafios e padronização.
Esse emplate foi disponibilizado na seguinte url: **[Acessar Template](https://github.com/Rocketseat/gostack-template-conceitos-nodejs)**

### Rotas da aplicação

A aplicação possui 5 rotas, sendo elas:

- **`POST /repositories`**: A rota deve receber `title`, `url` e `techs` dentro do corpo da requisição, sendo a URL o link para o github desse repositório. Ao cadastrar um novo projeto, ele deve ser armazenado dentro de um objeto no seguinte formato: `{ id: "uuid", title: 'Desafio Node.js', url: 'http://github.com/...', techs: ["Node.js", "..."], likes: 0 }`;

- **`GET /repositories`**: Rota que lista todos os repositórios;

- **`PUT /repositories/:id`**: A rota deve alterar apenas o `title`, a `url` e as `techs` do repositório que possua o `id` igual ao `id` presente nos parâmetros da rota;

- **`DELETE /repositories/:id`**: A rota deve deletar o repositório com o `id` presente nos parâmetros da rota;

- **`POST /repositories/:id/like`**: A rota deve aumentar o número de likes do repositório específico escolhido através do `id` presente nos parâmetros da rota, a cada chamada dessa rota, o número de likes deve ser aumentado em 1;


### Especificação para rodar a aplicação na sua máquina

Para rodar a aplicação na máquina local é necessário ter as seguintes aplicações instaladas na máquina, são elas:

- Node JS;
- Yarn;
- Git;

Tendo as aplicações instaladas, clone o projeto numa pasta local.

Após ter clonado o repositório em uma pasta local, acesse a mesma via terminal e rode o comando yarn dentro da pasta.

Esse comando fará com que todas as dependências do projeto sejam instaladas no arquivo package.json.

Tendo concluído isso, basta rodar o comando yarn dev que a aplicação estará rodando na porta 3333.


### Específicação dos testes

Essa aplicação já possui alguns testes configurados e eles podem ser encontrados na pasta src/__tests__

Caso você tenha dúvidas quanto ao que são os testes, e como interpretá-los, dé uma olhada em ** (https://github.com/Rocketseat/bootcamp-gostack-desafios/tree/master/faq-desafios).**

Para esse desafio foram escritos os seguintes testes:

- **`should be able to create a new repository`**: Para que esse teste passe, sua aplicação deve permitir que um repositório seja criado, e retorne um json com o projeto criado.

- **`should be able to list the repositories`**: Para que esse teste passe, sua aplicação deve permitir que seja retornado um array com todos os repositórios que foram criados até o momento.

- **`should be able to update repository`**: Para que esse teste passe, sua aplicação deve permitir que sejam alterados apenas os campos `url`, `title` e `techs`.

- **`should not be able to update a repository that does not exist`**: Para que esse teste passe, você deve validar na sua rota de update se o id do repositório enviado pela url existe ou não. Caso não exista, retornar um erro com status `400`.

- **`should not be able to update repository likes manually`**: Para que esse teste passe, você não deve permitir que sua rota de update altere diretamente os likes desse repositório, mantendo o mesmo número de likes que o repositório já possuia antes da atualização. Isso porque o único lugar que deve atualizar essa informação é a rota responsável por aumentar o número de likes.

- **`should be able to delete the repository`**: Para que esse teste passe, você deve permitir que a sua rota de delete exclua um projeto, e ao fazer a exclusão, ele retorne uma resposta vazia, com status `204`.

- **`should not be able to delete a repository that does not exist`**: Para que esse teste passe, você deve validar na sua rota de delete se o id do repositório enviado pela url existe ou não. Caso não exista, retornar um erro com status `400`.

- **`should be able to give a like to the repository`**: Para que esse teste passe, sua aplicação deve permitir que um repositório com o id informado possa receber likes. O valor de likes deve ser incrementado em 1 a cada requisição, e como resultado, retornar um json contendo o repositório com o número de likes atualizado.

- **`should not be able to like a repository that does not exist`**: Para que esse teste passe, você deve validar na sua rota de like se o id do repositório enviado pela url existe ou não. Caso não exista, retornar um erro com status `400`.

## :memo: Licença

Esse projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE.md) para mais detalhes.

---

Feito com 💜 by Rodrigo Abreu
