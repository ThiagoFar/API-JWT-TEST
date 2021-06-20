Prova Engenheiro de Software Jr


Tecnologias:


A API é escrita em JavaScript com Node.js 


Login usando autenticação JWT.


Mysql para gerenciar o banco.


FrontEnd usando React.js 



--------------------------------Instruções:--------------------------------

1 - Instalar o Node.Js https://nodejs.org/en/download/.

2 - alterar o arquivo  API-JWT-TEST\config.json colocando usuario e senha de um perfil local.

3 - Iniciar a API Executando no cmd o comando "npm install" (para instalar dependências) e em seguida "npm start" dentro de \API-JWT-TEST, a estrutura do banco é criada automaticamente nesse passo.

4 - Caso queira povoar o banco, faça o import do dados (Mysql Workbench) que estão em em: API-JWT-TEST\import_dados\Dump

5 - Caso queira vizualizar o exemplo de front end basta executar no cmd o comando "npm start" dentro de API-JWT-TEST\react frontend, a página em http://localhost:8080/login deve abrir automaticamente.

Link de um video rodando as funcionalidades básicas: https://www.youtube.com/watch?v=WAdSP-BesdU  (assistir em tela cheia).

--------------------------------Curl de requests exportado do Postman: --------------------------------

//1.Registrar usuário

	curl --location --request POST 'http://localhost:4000/users/register' \
	--header 'Content-Type: application/json' \
	--data-raw '{
		"firstName": "",
		"lastName": "",
		"cpf": " ",
		"username": "",
		"password": "",
		"cep": ""
	}'

//1.Exemplo de response

{"message":"Registration successful"}

  ------------------------------------------------------------------------------------------------
//2.Logar em usuário

	curl --location --request POST 'http://localhost:4000/users/authenticate' \
	--header 'Content-Type: application/json' \
	--data-raw '{
		"username": "",
		"password": ""
	}'

//2.Exemplo de response

	{
		"id": 7,
		"firstName": "John",
		"lastName": "Neumann",
		"cpf": "10000000000",
		"username": "john.neumann",
		"cep": "33679122",
		"createdAt": "2021-06-20T14:05:40.000Z",
		"updatedAt": "2021-06-20T14:05:40.000Z",
		"token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOjcsImlhdCI6MTYyNDE5Nzk0NiwiZXhwIjoxNjI0ODAyNzQ2fQ.RJVsGupFnz5r84ZpgQgajFbt_AFOnRNmFESVCZxmWng"
	}
------------------------------------------------------------------------------------------------
//3.Ver lista de usuários

curl --location --request GET 'http://localhost:4000/users'

//3.Exemplo de response

    {
        "id": 1,
        "firstName": "Enrico",
        "lastName": "Fermi",
        "cpf": "68421384532",
        "username": "enrico.fermi",
        "cep": "12345678910",
        "createdAt": "2021-06-20T11:46:21.000Z",
        "updatedAt": "2021-06-20T11:50:56.000Z"
    },
    {
        "id": 2,
        "firstName": "Richard",
        "lastName": "Feynman",
        "cpf": "49793100143",
        "username": "richard.feynman",
        "cep": "721150680",
        "createdAt": "2021-06-20T11:55:39.000Z",
        "updatedAt": "2021-06-20T11:56:16.000Z"
    },
    {
        "id": 3,
        "firstName": "Niels",
        "lastName": "Bohr",
        "cpf": "9066678372",
        "username": "niels.bohr",
        "cep": "69452689",
        "createdAt": "2021-06-20T11:59:44.000Z",
        "updatedAt": "2021-06-20T11:59:44.000Z"
    },

//4.Alterar um ou mais campos 

	curl --location --request PUT 'http://localhost:4000/users/7' \
	--header 'Content-Type: application/json' \
	--data-raw '{
		"cpf": "1445159746"
	}'

//4.Exemplo de response

	{
		"id": 7,
		"firstName": "John",
		"lastName": "Neumann",
		"cpf": "1445159746",
		"username": "john.neumann",
		"cep": "33679122",
		"createdAt": "2021-06-20T14:05:40.000Z",
		"updatedAt": "2021-06-20T14:06:22.628Z"
	}
	------------------------------------------------------------------------------------------------

Duvidas: thiagorodrigues@email.com  -  (61)999320640
