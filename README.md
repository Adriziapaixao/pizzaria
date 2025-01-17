# pizzaria

# Sistema de Gerenciamento de Pedidos

Este projeto é um sistema simples para gerenciar clientes, pedidos e pagamentos. Ele utiliza o Spring Framework para gerenciar as dependências e persistência de dados.

## UML

Abaixo está o diagrama UML representando as classes e seus relacionamentos:


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