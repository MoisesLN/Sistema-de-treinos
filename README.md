# Prova de flask
O README servirá apenas para responder as questões passadas na avaliação
## Por que as rotas de autenticação foram movidas para auth.py?
Por organização e modularização, que deixam o código mais manutenível.
## Como a aplicação identifica o usuário logado usando `session`?
Quando o usuário realiza o login, a session guarda seu id, e em qualquer página, para verificar se o usuário está logado, é só puxar se existe o id guardado na session.
## Como o código impede que um usuário acesse treinos de outro usuário?
Para isso, antes de mostrar os treinos, verificamos se o id do usuário logado bate com a chave estrangeira `usuario_id` da tabela treinos.