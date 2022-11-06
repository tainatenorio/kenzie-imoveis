
<h1> 
KImóveis -  um serviço de back-end responsável por gerenciar uma imobiliária utilizando TypeORM, PostgresSQL e TypeScript.

</h1>

<h2>Regras de negócio</h2>

Usuários
- A rota de criação de usuário deve retornar todos os dados, com exceção da hash de senha.
- Não podem ser cadastrados dois usuário com o mesmo e-mail.
- Para listar todos os usuários, a rota pode ser acessada apenas por administradores.
- Apenas administradores podem atualizar qualquer usuário, usuários não-administradores podem apenas atualizar seu próprio usuário.
- Realizar o soft delete do usuário, alterando isActive para false, não deve ser possível realizar um soft delete um usuário inativo, a rota pode ser acessada apenas por administradores.

Login
- Ao realizar o login deve validar se o usuário existe e validar se a senha está correta.

Categorias
- Ao criar uma nova categoria, não podem ser cadastradas duas categorias com o mesmo nome.
- Para listar todas as categorias a rota não precisa de autenticação para ser acessada.

Propriedades
- Ao criar uma nova propriedade, não podem ser cadastrados dois imóveis com o mesmo endereço.
- Não podem ser cadastrados imóveis com o campo state maior que 2 dígitos.
- Não podem ser cadastrados imóveis com o campo zipCode maior que 8 dígitos.

Agendamentos
- Para fazer um agendamento, não pode ser possível agendar uma visita a um imóvel com a mesma data e hora.
- Só deve ser possível agendar uma visita durante horário comercial (08:00 as 18:00).
- Só deve ser possível agendar uma visita durante em dias úteis (segunda à sexta).

Tecnologias usadas
- NodeJS
- ExpressJS
- TypeScript
- TypeORM
- PostgreSQL
- Jest
- padrão de arquitetura MVC
- Docker & docker-compose



















