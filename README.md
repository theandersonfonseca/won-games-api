<div align="center">
  <img src="./github/logo.png" width="100px"/>
</div>

Esta é a API criada para a Won Games, um e-commerce de jogos desenvolvido durante o curso de **[React Avançado do Willian Justen](https://www.udemy.com/course/react-avancado/)**

- **[Acesse o Repositório do Client](https://github.com/theandersonfonseca/won-games-client)**

---

## ⚙️ Rodando a API

Este projeto utiliza **[PostgreSQL](https://www.postgresql.org/)**, portanto, para fazê-lo funcionar, instale em sua máquina local ou use Docker.

A configuração do banco de dados pode ser encontrada em **[config/database.js](https://github.com/theandersonfonseca/won-games-api/blob/master/config/database.js)**

**Clone o repositório**

```
git clone https://github.com/theandersonfonseca/won-games-api.git
```

**Acesse a pasta do projeto**

```
cd won-games-api
```

**Instale as dependências**

```
yarn
```

**Inicie a api**

```
yarn develop
```

As urls para acessar são:

- `http://localhost:1337/admin` - O painel para criar e preencher dados
- `http://localhost:1337/graphql` - Playground GraphQL para testar suas queries

Na primeira vez para acessar o Admin, você precisará criar um usuário.

### Preenchendo dados

Este projeto utiliza a rota ` /games/populate` para preencher os dados por meio do site **[GoG](https://www.gog.com/)**. Para que funcione, siga os passos:

- Vá para Roles & Permissions > Public e certifique-se de que a rota `game:populate` está disponível ao público e o upload também

- Com o Strapi rodando, execute o seguinte comando em seu terminal:

```
$ curl -X POST http://localhost:1337/games/populate

# Você também pode passar parâmetros, como:
$ curl -X POST http://localhost:1337/games/populate?page=2
$ curl -X POST http://localhost:1337/games/populate?search=simcity
$ curl -X POST http://localhost:1337/games/populate?sort=rating&price=free
$ curl -X POST http://localhost:1337/games/populate?availability=coming&sort=popularity
```

---

Feito com 💜 por **[Anderson Fonseca](https://github.com/theandersonfonseca)**.
