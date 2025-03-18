🚀 Como Rodar o Projeto Localmente
1️⃣ Clonar o Repositório
git clone https://github.com/seu-usuario/nome-do-repositorio.git cd nome-do-repositorio

2️⃣ Configurar o Ambiente Garanta que você tem o Java 17+ e o Maven instalados. Se precisar instalar o Maven, siga a documentação oficial.

3️⃣ Rodar o Projeto Para iniciar o servidor, execute:

mvn spring-boot:run A aplicação será iniciada em http://localhost:8080 🚀

🛠️ Endpoints da API Aqui estão os principais endpoints da API e como testá-los no Postman ou cURL.

🔹 1. Listar Todos os Produtos 📌 GET /produtos

curl -X GET http://localhost:8080/produtos 🔹 2. Buscar Produto por ID 📌 GET /produtos/{id} curl -X GET http://localhost:8080/produtos/1

🔹 3. Criar um Novo Produto 📌 POST /produtos 📌 Body (JSON): { "nome": "Teclado Gamer", "preco": 250.0 } curl -X POST http://localhost:8080/produtos -H "Content-Type: application/json" -d '{"nome": "Teclado Gamer", "preco": 250.0}'

🔹 4. Atualizar um Produto 📌 PUT /produtos/{id} 📌 Body (JSON):

{ "nome": "Teclado Mecânico RGB", "preco": 300.0 }

curl -X PUT http://localhost:8080/produtos/1 -H "Content-Type: application/json" -d '{"nome": "Teclado Mecânico RGB", "preco": 300.0}'

🔹 5. Excluir um Produto 📌 DELETE /produtos/{id}

curl -X DELETE http://localhost:8080/produtos/1

🗄️ Acessar o Banco de Dados H2 O projeto usa H2 Database para armazenar os dados temporariamente. Para acessar o banco:

Inicie a aplicação (mvn spring-boot:run).

Abra no navegador:

http://localhost:8080/h2-console

Configuração de Acesso:

JDBC URL: jdbc:h2:mem:testdb Usuário: sa Senha: (deixe em branco) Execute a consulta para ver os produtos:

SELECT * FROM PRODUTOS; 👨‍🏫 Sobre o Projeto Este projeto faz parte das aulas de SOA e Web Services da FIAP e tem como objetivo ensinar os alunos a criar e consumir APIs REST com Spring Boot.

📌 Dúvidas? Sugestões? Entre em contato ou contribua no repositório! 🚀

🔍 Testar os endpoints no Postman
