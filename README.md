﻿# pizzaria

Este projeto é um sistema simples para gerenciar **clientes**, **pedidos** e **pagamentos**. Ele utiliza o **Spring Framework** para gerenciar as dependências e a persistência de dados, além de seguir boas práticas de desenvolvimento, como Clean Code e princípios RESTful.

## **Funcionalidades**
- Cadastro de clientes com validações de dados.
- Gerenciamento de pedidos vinculados aos clientes.
- Registro de pagamentos associados aos pedidos.
- Persistência de dados utilizando o banco de dados H2.

## UML

Abaixo está o diagrama UML representando as classes e seus relacionamentos:

## **Tecnologias Utilizadas**
- **Java 17**
- **Spring Boot 3.x**
- **Spring Data JPA**
- **H2 Database** (banco de dados em memória para desenvolvimento e testes)
- **Maven** (gerenciador de dependências)
- **Jakarta Persistence API** (JPA)

## **Endpoints Disponíveis**
-Clientes
POST /clientes: Cria um novo cliente.


```plaintext
+---------------------+ 1 N +--------------------------+ 1 1 +-------------------------+
| Cliente           |<----------| Pedido             |---------->| Pagamento           |
+-------------------+           +-------------------+           +----------------------+
| - id: Long        |           | - id: Long         |           | - id: Long          |
| - nome: String    |           | - descricao: String|           | - pedidoId: Long    |
| - email: String   |           | - clienteId: Long  |           | - formaPagamento:   |
|                   |           |                    |           |   String            |
|                   |           |                    |           | - valorPago: double |
|                   |           |                    |           | - dataHoraPagamento |
|                   |           |                    |           |   : LocalDate       |
+-------------------+           +--------------------+           +---------------------+

