# 🚀 Projeto API de CRUD de Documentos (docCrud)

Uma API REST simples para um CRUD (Create, Read, Update, Delete) de documentos e suas respectivas categorias. Este projeto foi desenvolvido em Java com Spring Boot.

## 🛠️ Tecnologias Utilizadas

* **Java 21**
* **Spring Boot 3**
* **Maven**
* **Spring Data JPA (Hibernate)**
* **Lombok**
* **Banco de Dados H2 (em memória)**
* **Springdoc (Swagger)** para documentação da API

## ▶️ Como Executar

1.  **Clone o repositório:**
    ```bash
    git clone [URL_DO_SEU_REPOSITORIO]
    cd docCrud
    ```

2.  **Compile o projeto com Maven:**
    ```bash
    mvn clean install
    ```

3.  **Execute a aplicação:**
    ```bash
    mvn spring-boot:run
    ```

A aplicação estará disponível em `http://localhost:8080`.

## 📚 Documentação (Swagger)

A documentação completa da API, gerada automaticamente pelo Springdoc (Swagger), pode ser acessada no seu navegador após iniciar a aplicação:

➡️ **[http://localhost:8080/swagger-ui.html](http://localhost:8080/swagger-ui.html)**

---

## 🗺️ Endpoints da API (Exemplos para Postman)

Aqui estão os principais endpoints da API e como usá-los no Postman.

### 📁 Recurso: Categorias

**URL Base:** `http://localhost:8080/api/categorias`

#### 1. Criar Categoria
* **Método:** `POST`
* **URL:** `http://localhost:8080/api/categorias`
* **Body (JSON):**
    ```json
    {
      "nome": "Financeiro"
    }
    ```

#### 2. Listar Todas as Categorias
* **Método:** `GET`
* **URL:** `http://localhost:8080/api/categorias`
* **Body:** (Nenhum)

#### 3. Buscar Categoria por ID
* **Método:** `GET`
* **URL:** `http://localhost:8080/api/categorias/1` (substitua `1` pelo ID desejado)
* **Body:** (Nenhum)

#### 4. Atualizar Categoria
* **Método:** `PUT`
* **URL:** `http://localhost:8080/api/categorias/1` (substitua `1` pelo ID desejado)
* **Body (JSON):**
    ```json
    {
      "nome": "Relatórios Financeiros"
    }
    ```

#### 5. Deletar Categoria
* **Método:** `DELETE`
* **URL:** `http://localhost:8080/api/categorias/1` (substitua `1` pelo ID desejado)
* **Body:** (Nenhum)

---

### 📄 Recurso: Documentos

**URL Base:** `http://localhost:8080/api/documentos`

#### 1. Criar Documento
* **Método:** `POST`
* **URL:** `http://localhost:8080/api/documentos`
* **Body (JSON):** (Nota: A categoria com `id: 1` deve existir primeiro)
    ```json
    {
      "titulo": "Relatório Anual 2025",
      "conteudo": "Documento contendo o balanço financeiro do ano.",
      "categoria": {
        "id": 1
      }
    }
    ```

#### 2. Listar Todos os Documentos
* **Método:** `GET`
* **URL:** `http://localhost:8080/api/documentos`
* **Body:** (Nenhum)

#### 3. Buscar Documento por ID
* **Método:** `GET`
* **URL:** `http://localhost:8080/api/documentos/1` (substitua `1` pelo ID desejado)
* **Body:** (Nenhum)

#### 4. Atualizar Documento
* **Método:** `PUT`
* **URL:** `http://localhost:8080/api/documentos/1` (substitua `1` pelo ID desejado)
* **Body (JSON):**
    ```json
    {
      "titulo": "Relatório Anual 2025 (Revisado)",
      "conteudo": "Conteúdo atualizado.",
      "categoria": {
        "id": 1
      }
    }
    ```

#### 5. Deletar Documento
* **Método:** `DELETE`
* **URL:** `http://localhost:8080/api/documentos/1` (substitua `1` pelo ID desejado)
* **Body:** (Nenhum)