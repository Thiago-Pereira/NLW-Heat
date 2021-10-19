# NLW-Heat-Node

Projeto realizado na NLW Heat na aula de Node JS para criar uma aplicação que se autentica no gitub e retorna suas informações, 
utiliazando o Express, Prisma, SQLite e também criando o socket com o Socket IO para juntar com as aplicações que serão feitas nas próximas aulas.

## Rotas

# /authenticate

Pede para o usuário logar no github, caso seja primeiro acesso ao projeto, e guarda essas informações no banco.

Após isso gera um token para o usuário se autenticar em outras rotas que erão descritas abaixo.

# /messages

Envia uma mensagem para ser salva no DB, e salva a mesma com as informações do usuário que a enviou. 

Para o acesso é necessário usar o token obtido na rota authenticate.

# /messages/last3

Busca no DB as últimas 3 mensagens salvas e os usuários que as salvaram.

Não necessita do Token

# /profile

Busca as informações do usuaário salvas no DB, usando o token que contem o id do usuário.
