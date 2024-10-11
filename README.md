Descrição do Projeto:
Este projeto consiste em um backend Java Spring que permite o gerenciamento de medicamentos cadastrados. É possível listar todos os medicamentos, buscar um medicamento pelo ID e adicionar novos medicamentos, com as informações de nome, descrição, quantidade e preço.

Como executar o projeto
Pré-requisitos
Java JDK 17 ou superior
Maven (ou use a ferramenta integrada à sua IDE)
Postman ou outro software para testes de APIs REST

#### Passos para rodar a aplicação localmente:

1. **Clone o repositório:**

   ```bash
   git clone https://github.com/GabrielVinhati/CrudFarmacia
   ```

2. **Compile e rode o projeto:**

   Se estiver usando o Maven, utilize o seguinte comando:

   ```bash
   mvn spring-boot:run
   ```

   Ou rode a aplicação diretamente pela sua IDE de preferência (como IntelliJ ou Eclipse).

3. **Acesse a aplicação:**

   O projeto será executado na URL: `http://localhost:8080`.

---

### Endpoints Disponíveis

#### Listar todos os usuários:

- **Método:** GET
- **URL:** `/api/items`
- **Exemplo de resposta:**

  ```json
  [
    {
        "id": 1,
        "name": "Paracetamol",
        "description": "Um fármaco com propriedades analgésicas e antipiréticas utilizado essencialmente para tratar a febre e a dor leve e moderada",
        "quantity": 20,
        "price": 10.99
      }
    },
    {
      "id": 2,
        "name": "Nimesulida",
        "description": "A nimesulida é um anti-inflamatório usado para aliviar dor e inflamação, com ação rápida, mas pode causar efeitos colaterais gastrointestinais e hepáticos.",
        "quantity": 10,
        "price": 9.78
      }
    }
  ]
  ```

#### Buscar um medicamento pelo ID:

- **Método:** GET
- **URL:** `/api/items/id}`
- **Exemplo de resposta:**
'http://localhost:8080/api/items/2'
  ```json
   {
      "id": 2,
        "name": "Nimesulida",
        "description": "A nimesulida é um anti-inflamatório usado para aliviar dor e inflamação, com ação rápida, mas pode causar efeitos colaterais gastrointestinais e hepáticos.",
        "quantity": 10,
        "price": 9.78
      }
  ```

#### Inserir um novo usuário:

- **Método:** POST
- **URL:** `http://localhost:8080/api/items/`
- **Body (JSON):**

  ```json
  {
        "name": "Bromoprida",
        "description": "A bromoprida é um antiemético e regulador da motricidade gastroduodenal que estimula o peristaltismo gástrico a partir do centro, promovendo ativamente o esvaziamento do estômago.",
        "quantity": 10,
        "price": 13.95
      }
  }
  ```

- **Exemplo de resposta:**

  ```json
  {
    "id": 3,
    "name": "Bromoprida",
    "description": "A bromoprida é um antiemético e regulador da motricidade gastroduodenal que estimula o peristaltismo gástrico a partir do centro, promovendo ativamente o esvaziamento do estômago.",
    "quantity": 10,
    "price": 13.95
    }
  }
  ```
