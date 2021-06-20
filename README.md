Prova Engenheiro de Software Jr

Tecnologias:

a API é escrita em JavaScript com Node.js 

login usando autenticação JWT.

Mysql para gerenciar o banco.

Exemplo de frontEnd usando React.js 

Instruções:

1 - Instalar o Node.Js https://nodejs.org/en/download/.

2 - alterar o arquivo  API-JWT-TEST\config.json colocando usuario e senha de um perfil local.

3 - Iniciar a API Executando no cmd o comando "npm install" (para instalar dependências) e em seguida "npm start" dentro de \API-JWT-TEST, a estrutura do banco é criada automaticamente nesse passo.

4 - Caso queira povoar o banco, faça o import do dados (Mysql Workbench) que estão em em: API-JWT-TEST\import_dados\Dump

5 - Caso queira vizualizar o exemplo de front end basta executar no cmd o comando "npm start" dentro de API-JWT-TEST\react frontend, a página em http://localhost:8080/login deve abrir automaticamente.

Link de um video rodando as funcionalidades básicas: https://www.youtube.com/watch?v=WAdSP-BesdU  (assistir em tela cheia).

Curl de requests exportado do Postman:

//Registrar usuário
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

//Logar em usuário
curl --location --request POST 'http://localhost:4000/users/authenticate' \
--header 'Content-Type: application/json' \
--data-raw '{
    "username": "",
    "password": ""
}'

//Ver lista de usuários
curl --location --request GET 'http://localhost:4000/users'

//Alterar um ou mais campos 
curl --location --request PUT 'http://localhost:4000/users/7' \
--header 'Content-Type: application/json' \
--data-raw '{
    "cpf": "1445159746"
}'




Duvidas: thiagorodrigues@email.com  -  (61)999320640
