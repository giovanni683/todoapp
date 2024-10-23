# Resumo do Meu Processo de Desenvolvimento e Teste da Aplicação Spring Boot

## 1. Configuração do Projeto Spring Boot

- **IDE (IntelliJ/Eclipse)**: Comecei criando um projeto Spring Boot, que é uma estrutura de aplicação Java que utilizo para desenvolver serviços web e aplicações empresariais. A IDE facilita a codificação, depuração e gerenciamento do projeto.

- **Dependências**: Usei o Maven para gerenciar as dependências do projeto, incluindo a biblioteca Spring Boot e o H2 Database para persistência de dados.

- **Estrutura do Projeto**:
  - `src/main/java`: Código-fonte Java da minha aplicação.
  - `src/main/resources`: Recursos como arquivos de configuração (`application.properties`), onde defini a configuração da minha aplicação e do banco de dados.

## 2. Desenvolvimento da API

- **Model**: Criei uma classe `User` que representa um usuário no sistema, parte do modelo de dados que a aplicação manipulará.

- **Repositório**: Desenvolvi uma interface `UserRepository` que estende `JpaRepository`, permitindo interações com o banco de dados, como operações de CRUD (Create, Read, Update, Delete) para usuários.

- **Controlador**: Criei uma classe `UserController` que define os endpoints da minha API. Cada método nessa classe é mapeado para uma URL específica e um método HTTP (GET, POST, DELETE).

## 3. Configuração do Banco de Dados H2

- **Banco de Dados H2**: Configurei o H2 como um banco de dados em memória, permitindo armazenar dados temporariamente durante o desenvolvimento e testes, sem precisar de um banco de dados externo.

- **application.properties**: Especifiquei configurações como o nome da aplicação, a URL do banco de dados e as credenciais.

## 4. Executando a Aplicação

- **Rodando a Aplicação**: Executei a classe principal (`TodoappApplication`) para iniciar o servidor embutido (Tomcat) que hospeda minha aplicação.

- **Verificação de Status**: No console da IDE, verifiquei se a aplicação estava rodando na porta 8080, indicando que a API estava disponível para receber requisições.

## 5. Testando a API com o Postman

- **Postman**: Utilize essa ferramenta para testar a API, enviando requisições HTTP e visualizando as respostas da minha aplicação.

### Testes Realizados:

- **GET /api/users**: Obtive todos os usuários. Inicialmente, recebi um JSON vazio (`[]`).
- **POST /api/users**: Criei um novo usuário. Enviei dados de um usuário e recebi uma resposta com os detalhes do usuário criado.
- **GET /api/users/{id}**: Obtive um usuário específico pelo ID e verifiquei os detalhes do usuário que havia criado.
- **DELETE /api/users/{id}**: Deletei um usuário específico e a resposta indicou que a operação foi bem-sucedida.

## Objetivos e Benefícios de Cada Etapa

- **Estrutura e Organização**: O Spring Boot proporciona uma maneira organizada de desenvolver aplicações, facilitando a manutenção e escalabilidade.
- **Persistência de Dados**: Utilizar um banco de dados em memória (H2) simplifica o desenvolvimento e testes, sem complicações.
- **Testabilidade**: O uso do Postman permite testar a API rapidamente, garantindo que as funcionalidades funcionem conforme o esperado antes de passar para um ambiente de produção.
- **Desenvolvimento Ágil**: As ferramentas e práticas utilizadas permitem um desenvolvimento mais rápido e eficiente, focando na entrega de valor ao usuário final.

## Conclusão

Esse processo integrou várias ferramentas e práticas de desenvolvimento, desde a configuração do projeto até o teste da API. Ele me permite criar, testar e iterar rapidamente em minhas aplicações, preparando-me para desenvolver software de forma profissional.
