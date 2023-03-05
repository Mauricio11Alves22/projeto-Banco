### Banco dindin

realizei um projeto em dupla no curso da cubos academy onde precisavamos fazer diversas operações bancarias como cadastro, login, transações, exclusão e etc...
tomei a liberdade de realizar o mesmo projeto individualmente para testar meu conhecimento.

* Criamos um banco de dados com 3 tabelas para receber todos os dados necessarios da nossa API
* começa o codigo pelo cadastro de usuario onde tem que ser informado, nome, email que não exista ainda no banco de dados, e senha que é criptografada antes de ser salva no banco de dados, criei intermediários para verificar se foram informados todos os campos, de maneira que pudessem ser reutilizados em outros endpoints.
* Segundo é o login onde o é informado email e senha, o email desta vez tem que retornar true, e a senha tem que conferir com a senha criptografada, com o login concluido o sistema gera um token valido por 8 horas onde ele servirá para todas as novas operações e o úsuario poderá fazer operações em sua própria conta, contendo dentro dele o id do úsuario.
* Para detalhar úsuario, listar categorias e listar transações apenas necessitamos do token valido mais a rota especifica.
* Para atualizar o úsuario, precisamos ver se foi informado, nome, email e senha, a o email não pode ser um email ja cadastrado para efetuar a alteração do úsuario.
* Para detalhar uma operação expecifica o úsuario deve digitar a rota mais o id da transação que recebe como params.
* Para cadastrar uma transação verificamos camppos obrigatórios, descrição, valor, data, categoria e tipo de transação, foi criando intermediário aqui tambem para validar em mais de um endpoint.
* Para realizar atualização da transação fazemos as mesmas validações de uma transação, para poder alterar no banco de dados.
* Para excluir uma transação usamos a rota mais o id passado, e recuperamos como params.
* Para obter o extrato de uma conta precisamos apenas do token válido.
* E por fim o extra que filtrar uma transação pela categoria inserida em obter uma transação, ela contém dois campos query params.

todos codigo tem respostas, Rest com status, usado try/catch para capturar mensagem de erros, o token recebido através do bearer token.
