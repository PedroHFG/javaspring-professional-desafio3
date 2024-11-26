# 🛠️ CRUD de Clientes com Spring Boot

Este projeto faz parte de um desafio do curso **Java Spring Professional** da [DevSuperior](https://devsuperior.com.br/). O objetivo é fazer uma aplicação Spring Boot com um CRUD completo de web services REST para gerenciar um recurso de clientes. O sistema oferece operações básicas como criação, leitura, atualização e exclusão (CRUD) e inclui validações e tratamento de exceções.

## 📋 Descrição do Projeto

O projeto é um desafio prático que implementa as seguintes funcionalidades:

- **Busca paginada de clientes**.
- **Busca de cliente por ID**.
- **Inserção de um novo cliente**.
- **Atualização de um cliente existente**.
- **Exclusão de um cliente**.

Além disso:

- O banco de dados H2 é usado para testes e persistência.
- Um seed inicial de pelo menos 10 clientes é configurado.
- Validações e tratamento de exceções estão implementados, garantindo respostas adequadas para erros.

## ⚙️ Funcionalidades

- **CRUD completo de clientes**:

  - Listagem de clientes com paginação.
  - Busca de cliente pelo ID.
  - Inserção de novos clientes.
  - Atualização de clientes existentes.
  - Exclusão de clientes pelo ID.

- **Validações**:

  - Nome não pode ser vazio.
  - Data de nascimento não pode ser futura.

- **Tratamento de Exceções**:
  - Retorno 404 (Not Found) para IDs não encontrados.
  - Retorno 422 (Unprocessable Entity) para erros de validação, com mensagens customizadas.

## 🛠️ Tecnologias Utilizadas

- **Java 21**
- **Spring Boot**
- **Maven**
- **Spring Data JPA**
- **H2 Database**
- **Spring Web**

## ⚙️ Pré-requisitos

- Java JDK 21 ou superior
- Maven
- Spring Boot

## 🚀 Como Executar o Projeto

1. Clone o repositório:

   ```bash
   git clone https://github.com/PedroHFG/javaspring-professional-desafio3
   ```

2. Navegue até a pasta do projeto:

   ```bash
   cd javaspring-professional-desafio3
   ```

3. Compile o projeto Maven:

   ```bash
   mvn clean install
   ```

4. Execute a aplicação

   ```bash
   mvn spring-boot:run
   ```

5. Acesse o H2 Console. O banco de dados H2 estará disponível no navegador. Acesse-o através do link:

   ```bash
   http://localhost:8080/h2-console
   ```

## 📦 Seeding de Dados

Os dados iniciais são inseridos automaticamente no banco de dados ao iniciar a aplicação, utilizando o arquivo import.sql. As tabelas esperadas, com seus relacionamentos, serão criadas corretamente e preenchidas com dados de exemplo.

## 🗄️ Configuração do Banco de Dados

O projeto utiliza o H2 Database em modo memória. As configurações podem ser encontradas no arquivo application.properties:

```bash
   # Dados de conexão com o banco H2
   spring.datasource.driverClassName=org.h2.Driver
   spring.datasource.url=jdbc:h2:mem:testdb
   spring.datasource.username=sa
   spring.datasource.password=
   # H2 Client
   spring.h2.console.enabled=true
   spring.h2.console.path=/h2-console
   # JPA, SQL
   spring.jpa.database-platform=org.hibernate.dialect.H2Dialect
   spring.jpa.defer-datasource-initialization=true
   spring.jpa.show-sql=true
   spring.jpa.properties.hibernate.format_sql=true
```

## 📞 Contato

Se você tiver dúvidas ou sugestões sobre o projeto, sinta-se à vontade para entrar em contato:

- **Email**: pedrohfidg@gmail.com
- **GitHub**: [PedroHFG](https://github.com/PedroHFG)
