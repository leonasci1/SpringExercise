SpringExercise 🚀
Uma aplicação de exemplo construída com Java e Spring Boot que expõe endpoints REST para operações de saudação e manipulação de usuários, utilizando um banco de dados MySQL.

✨ Tecnologias Utilizadas
Java 17+
Spring Boot
Maven
MySQL
Lombok
🔧 Configuração e Instalação
Siga os passos abaixo para configurar e executar o projeto localmente.

Pré-requisitos
Java 17 (ou superior) instalado.
Maven instalado.
MySQL Server rodando.
1. Banco de Dados
Antes de iniciar a aplicação, crie o banco de dados springexercise no seu MySQL.

SQL

CREATE DATABASE springexercise;
As credenciais e a URL de conexão podem ser ajustadas no arquivo src/main/resources/application.properties:

Properties

spring.datasource.url=jdbc:mysql://localhost:3306/springexercise
spring.datasource.username=root
spring.datasource.password=root
2. Configurações da Aplicação
A aplicação utiliza o perfil development por padrão e roda na porta 3000, conforme definido em application.properties:

Properties

# Perfil ativo da aplicação
spring.profiles.active=development

# Porta do servidor
server.port=3000
▶️ Como Rodar a Aplicação
Clone o repositório:

Bash

git clone <url-do-seu-repositorio>
cd SpringExercise
Instale as dependências com o Maven:

Bash

mvn clean install
Inicie a aplicação:

Bash

mvn spring-boot:run
A aplicação estará disponível em http://localhost:3000.

API Endpoints ⚡
Você pode testar os endpoints utilizando ferramentas como Postman, Insomnia ou cURL.

Saudação Simples
Retorna uma mensagem de saudação padrão.

Endpoint: GET /leandremo/get
Exemplo de Resposta:
Hello Leandro
Criar Usuário e Retornar Saudação
Recebe um JSON com os dados de um usuário e retorna uma mensagem personalizada.

Endpoint: POST /leandremo
Corpo da Requisição (JSON):
JSON

{
  "name": "Leandro",
  "email": "leandro@email.com"
}
Exemplo de Resposta:
Hello Leandro, your email is leandro@email.com
📂 Estrutura do Projeto
.
└── src/main/java/com/leandremo/SpringExercise/
    ├── SpringExerciseApplication.java  // Classe principal que inicia a aplicação
    ├── controller/
    │   └── Controller.java             // Define os endpoints REST
    ├── domain/
    │   └── User.java                   // Modelo de dados do usuário
    └── service/
        └── HelloWorldService.java      // Contém a lógica de negócio
