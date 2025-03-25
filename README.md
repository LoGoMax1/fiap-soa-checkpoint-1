🚀 Como Rodar o Projeto Localmente

2️⃣ Configurar o Ambiente Garanta que você tem o Java 17+ e o Maven instalados. Se precisar instalar o Maven, siga a documentação oficial.

3️⃣ Rodar o Projeto Para iniciar o servidor, execute:

mvn spring-boot:run A aplicação será iniciada em http://localhost:8080 🚀

🛠️ Endpoints da API Aqui estão os principais endpoints da API e como testá-los no Postman ou cURL.

🔹 1. Listar Todos os Pedidos 📌 GET /pedidos

curl -X GET http://localhost:8080/pedidos 🔹 2. Buscar Produto por ID 📌 GET /pedidos/{id} curl -X GET http://localhost:8080/pedidos/1

🔹 3. Criar um Novo Produto 📌 POST /pedidos 📌 Body (JSON): { "clienteNome": "Teclado Gamer", "valorTotal": 250.0 } curl -X POST http://localhost:8080/pedidos -H "Content-Type: application/json" -d '{"clienteNome": "Teclado Gamer", "valorTotal": 250.0}'

🔹 4. Atualizar um Produto 📌 PUT /pedidos/{id} 📌 Body (JSON):

{ "clienteNome": "Teclado Mecânico RGB", "valorTotal": 300.0 }

curl -X PUT http://localhost:8080/pedidos/1 -H "Content-Type: application/json" -d '{"clienteNome": "Teclado Mecânico RGB", "valorTotal": 300.0}'

🔹 5. Excluir um Produto 📌 DELETE /pedidos/{id}

curl -X DELETE http://localhost:8080/pedidos/1

🗄️ Acessar o Banco de Dados H2 O projeto usa H2 Database para armazenar os dados temporariamente. Para acessar o banco:

Inicie a aplicação (mvn spring-boot:run).

Abra no navegador:

http://localhost:8080/h2-console

Configuração de Acesso:

JDBC URL: jdbc:h2:mem:testdb Usuário: sa Senha: (deixe em branco) Execute a consulta para ver os pedidos:

SELECT * FROM pedidos; 👨‍🏫 Sobre o Projeto Este projeto faz parte das aulas de SOA e Web Services da FIAP e tem como objetivo ensinar os alunos a criar e consumir APIs REST com Spring Boot.

# listagem dos pedidos 

![Listagem dos Pedidos](.img\list.png)

# Adicionar pedidos

![Adicionar Pedidos](img\add.png)

# Pegar um pedido

![Pegar 1 Pedidos](img\get1.png)

# Update um pedido

![Atualizar 1 pedido](img\update.png)

# Deletar um pedido

![Deletar 1 pedido](img\delete.png)


