# Html - Verbos

GET - Buscar Dado
POST - Criar Dado
PUT/PATCH - Editar dado
DELETE - Deletar Dados

## #BackEnd
Possui 2 Duas Camadas

## 1° Camada - Controller
É responsável por receber as requisições dos clientes (geralmente via HTTP), validar os dados de entrada, chamar os serviços necessários e devolver a resposta ao cliente. Atua como intermediário entre a interface externa e a lógica interna da aplicação.

## 2° Camada - Services
Contém a lógica de negócios da aplicação. Ele processa as regras e operações necessárias, acessa dados e retorna os resultados ao Controller. O Service mantém o código organizado e separado das responsabilidades de manipulação de requisições.

Por convenção, cria-se duas pastas distintas para separar as requests dos services

## /services.js/user.js
Terá as funções para criar, editar e deletar os dados.

## /controller.js/user.js
Terá a função de criar as rotas que serão chamadas pelo http, e direcionar para o service requerido
necessita do import do router, e importar o arquivo js dos services para referencia-los em cada rota

Ao criar os dados no POST, para o terminal retorna-los sem erro, necessitara da biblioteca 'body-parser' no index.js e dessa forma chamar a função 
### app.use(bodyParser.json())
Quando fazer a requisição post, o erro de 'undenfined' sera sanado e apresentará a lista dos dados criados no post