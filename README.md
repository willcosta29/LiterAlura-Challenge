### LiteAlura 📚📚

**LiteAlura** é uma biblioteca desenvolvida em Java utilizando o framework Spring Boot. A biblioteca tem como principais funcionalidades buscar livros de uma API externa, salvar esses livros em um banco de dados PostgreSQL e permitir que os usuários interajam com esses dados através de um menu.

#### Requisitos de Sistema 💻

- **Java**: Versão 21 ou superior
- **Maven**: Para gerenciamento de dependências
- **PostgreSQL**: Para armazenamento de dados

#### Dependências Principais

- **Spring Boot Starter Data JPA**: Fornece integração com JPA e Spring Data.
- **PostgreSQL**: Driver JDBC para conexão com o banco de dados PostgreSQL.
- **Spring Boot Starter Test**: Conjunto de ferramentas para testar aplicações Spring Boot.
- **Jackson Databind**: Biblioteca para serialização e desserialização de objetos Java para JSON e vice-versa.
- **Jackson Core**: Biblioteca principal do Jackson para processamento JSON.

No Maven, adicione as seguintes dependências ao seu `pom.xml`:

```xml
<dependencies>
    <dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-data-jpa</artifactId>
    </dependency>
    <dependency>
        <groupId>org.postgresql</groupId>
        <artifactId>postgresql</artifactId>
        <scope>runtime</scope>
    </dependency>
    <dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-test</artifactId>
        <scope>test</scope>
    </dependency>
    <dependency>
        <groupId>com.fasterxml.jackson.core</groupId>
        <artifactId>jackson-databind</artifactId>
        <version>2.16.0</version>
    </dependency>
    <dependency>
        <groupId>com.fasterxml.jackson.core</groupId>
        <artifactId>jackson-core</artifactId>
        <version>2.16.0</version>
    </dependency>
</dependencies>
```

### Recursos Utilizados

Spring Boot Data JPA: Para facilitar a integração com o banco de dados utilizando JPA.
PostgreSQL: Banco de dados utilizado para armazenar os dados dos livros e autores.
Jackson: Para manipulação de dados JSON ao interagir com a API externa.
Estrutura do Projeto
com.litealura.model

Contém as classes de modelo, incluindo Livro e Autor.
com.litealura.repository

Contém as interfaces de repositório para LivroRepository e AutorRepository.
com.litealura.service

Contém as classes de serviço, incluindo LivroService que é responsável por buscar e salvar livros.
com.litealura.controller

Contém os controladores REST para lidar com as requisições HTTP.
Funcionalidades da Aplicação
A aplicação principal oferece as seguintes funcionalidades:

Buscar Livros pelo Título:

Realiza uma busca na API externa pelo título dos livros e salva os resultados no banco de dados.
Listar Livros Registrados:

Retorna uma lista de todos os livros salvos no banco de dados.
Listar Autores Registrados:

Retorna uma lista de todos os autores salvos no banco de dados.
Listar Autores Vivos:

Retorna uma lista de autores que ainda estão vivos.
Listar Autores Vivos com Filtro Refinado:

Retorna uma lista de autores vivos com filtros adicionais aplicados.
Listar Autores por Ano de Morte:

Retorna uma lista de autores filtrados pelo ano de morte.
Listar Livros por Idioma:

Retorna uma lista de livros filtrados pelo idioma.
