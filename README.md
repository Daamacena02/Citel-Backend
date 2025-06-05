# Citel Backend

Backend desenvolvido em Spring Boot para a aplicação Citel, que oferece APIs REST para gerenciamento de dados.

## Tecnologias usadas

- Java 21
- Spring Boot 3.3.4
- Spring Web (API REST)
- Spring Data JPA (integração com banco de dados)
- MySQL (banco de dados relacional)
- Lombok (redução de código boilerplate)
- Springdoc OpenAPI (documentação da API)
- JUnit (testes)

## Funcionalidades principais

- API REST para operações CRUD com persistência em banco MySQL
- Documentação automática da API via OpenAPI (Swagger UI)
- Integração com banco MySQL via Spring Data JPA

## Como rodar localmente

### Pré-requisitos

- Java 21 instalado
- MySQL instalado e configurado
- Maven instalado (ou use o wrapper do Maven que já vem no projeto)

### Passos

1. Clone o repositório:
   ```bash
   git clone https://github.com/Daamacena02/citel-back-end.git

2. Entre na pasta do projeto:
   cd citel-back-end

3. Configure o banco de dados:
* Crie um banco no MySQL (citel_db)
  
* Rode o Script abaixo para criar a tabela usuarios:
  
CREATE TABLE usuarios (
    id BIGINT AUTO_INCREMENT PRIMARY KEY,
    nome VARCHAR(255) NOT NULL,
    cpf VARCHAR(20) NOT NULL,
    rg VARCHAR(20) NOT NULL,
    data_nasc VARCHAR(20) NOT NULL,
    sexo VARCHAR(20) NOT NULL,
    mae VARCHAR(255) NOT NULL,
    pai VARCHAR(255) NOT NULL,
    email VARCHAR(255) NOT NULL,
    cep VARCHAR(20),
    endereco VARCHAR(255),
    numero INT,
    bairro VARCHAR(100),
    cidade VARCHAR(100),
    estado VARCHAR(50),
    telefone_fixo VARCHAR(20),
    celular VARCHAR(20),
    altura DOUBLE NOT NULL,
    peso DOUBLE NOT NULL,
    tipo_sanguineo VARCHAR(5)
);

* No arquivo src/main/resources/application.properties (ou .yml), configure as credenciais e URL do banco, exemplo:
  
   spring.application.name=citel
   spring.datasource.url=jdbc:mysql://localhost:3306/citel_db?useSSL=false&serverTimezone=UTC
   spring.datasource.username=root
   spring.datasource.password=teste

4. Rode a aplicação

5. Acesse a API em http://localhost:8080/swagger-ui.html

6. Envie o JSON fornecido pela Citel no endpoint a seguir:
   user-controller - POST /users

7. Após enviar o JSON, direcionar para o projeto do font-end em: 
