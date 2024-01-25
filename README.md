Bem-vindo ao repositório do projeto API de Receitas!

## Conclusão do Projeto

### 🚀 Projeto de Estudos em ASP.NET

Este projeto foi desenvolvido como parte de um estudo em ASP.NET. Durante o processo, foi possível aprimorar habilidades relacionadas ao funcionamento do ASP.NET, integração com C#, compreensão da arquitetura MVC e criação de controllers que seguem boas práticas. O objetivo era atender aos requisitos estabelecidos, e fico satisfeito em informar que 100% dos requisitos foram concluídos com sucesso.

### 📝 Habilidades Trabalhadas

Durante o projeto, foram trabalhadas as seguintes habilidades:

- Entendimento do funcionamento do ASP.NET e sua integração com C#.
- Compreensão da arquitetura MVC.
- Criação de controllers que recebem dados pelo corpo e pela URL da requisição.
- Implementação de códigos de retorno seguindo o padrão do HTTP Status Code.

## Endpoints

A API disponibiliza os seguintes endpoints:

### 1. **Listar Todas as Receitas**

- **URL:** `/recipe`
- **Método:** GET
- **Descrição:** Retorna todas as receitas disponíveis.

### 2. **Consultar Receita por Nome**

- **URL:** `/recipe/:name`
- **Método:** GET
- **Descrição:** Retorna uma receita específica consultando pelo nome.

### 3. **Adicionar Nova Receita**

- **URL:** `/recipe`
- **Método:** POST
- **Descrição:** Adiciona uma nova receita.
- **Corpo da Requisição:**
  ```json
  {
    "Name": "Nome da Receita",
    "RecipeType": 0,
    "PreparationTime": "0.2",
    "Ingredients": ["Ingrediente 1", "Ingrediente 2"],
    "Directions": "Passo a passo...",
    "Rating": "9"
  }

### 4. **Atualizar Receita**

- **URL:** `/recipe`
- **Método:** PUT
- **Descrição:** Atualiza uma receita existente.
- **Corpo da Requisição:**
  ```json
  {
    "Name": "Nome da Receita",
    "RecipeType": 0,
    "PreparationTime": "0.2",
    "Ingredients": ["Ingrediente 1", "Ingrediente 2"],
    "Directions": "Passo a passo...",
    "Rating": "9"
  }

### 5. **Remover Receita por Nome**

- **URL:** `/recipe/:name`
- **Método:** DELETE
- **Descrição:** Remove uma receita específica consultando pelo nome.
- **Resultado da Requisição:**
  - **Status HTTP:**
    - `204` (Sem conteúdo) em caso de sucesso.
    - `404` se nenhuma receita for encontrada.

### 6. **Consultar Usuário por Email**

- **URL:** `/user/:email`
- **Método:** GET
- **Descrição:** Retorna informações de um usuário consultando pelo email.
- **Resultado da Requisição:**
  - **Status HTTP:**
    - `200` com o usuário correspondente.
    - `404` se nenhum usuário for encontrado.

### 7. **Adicionar Novo Usuário**

- **URL:** `/user`
- **Método:** POST
- **Descrição:** Adiciona um novo usuário.
- **Corpo da Requisição:**
  ```json
  {
    "email": "email@example.com",
    "name": "Nome do Usuário",
    "password": "SenhaSegura123"
  }

- **Exemplo de Requisição:**
  ```bash
  curl -X POST -H "Content-Type: application/json" -d '{"email": "email@example.com", "name": "Nome do Usuário", "password": "SenhaSegura123"}' http://seu-domino.com/user


- **Exemplo de Resposta:**
  ```json
  {
  "email": "email@example.com",
  "name": "Novo Nome do Usuário",
  "password": "NovaSenha456"
  }

### 8. **Atualizar Usuário por Email**

- **URL:** `/user/:email`
- **Método:** PUT
- **Descrição:** Atualiza informações de um usuário existente.
- **Corpo da Requisição:**
  ```json
  {
    "email": "email@example.com",
    "name": "Novo Nome do Usuário",
    "password": "NovaSenha456"
  }

### 9. **Remover Usuário por Email**

- **URL:** `/user/:email`
- **Método:** DELETE
- **Descrição:** Remove um usuário consultando pelo email.

### 10. **Adicionar Comentário**

- **URL:** `/comment`
- **Método:** POST
- **Descrição:** Adiciona um comentário a uma receita.
- **Corpo da Requisição:**
  ```json
  {
    "Email": "email@example.com",
    "RecipeName": "Nome da Receita",
    "CommentText": "Comentário interessante..."
  }

### 11. **Consultar Comentários por Nome da Receita**

- **URL:** `/comment/:recipeName`
- **Método:** GET
- **Descrição:** Retorna todos os comentários associados a uma receita consultando pelo nome.
