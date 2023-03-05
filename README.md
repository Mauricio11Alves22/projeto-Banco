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

![Sem título](https://user-images.githubusercontent.com/91357497/222984032-4581e107-0420-4e3e-a763-f3c4d8a47ab7.jpg)
![Sem título2](https://user-images.githubusercontent.com/91357497/222984037-3e913dc5-cefe-4966-8639-d650c5c8ac04.jpg)
![Sem título3](https://user-images.githubusercontent.com/91357497/222984038-d9f13993-3a1b-4f3e-bd2f-e55c7c15a114.jpg)
![Sem título4](https://user-images.githubusercontent.com/91357497/222984040-81d2511c-797a-4553-ad3a-6ea481f16dec.jpg)
![Sem título5](https://user-images.githubusercontent.com/91357497/222984042-a3e41c25-379f-4080-890b-523b656a5d2b.jpg)
![Sem título6](https://user-images.githubusercontent.com/91357497/222984043-ad6e4b3d-1269-47f7-b9e8-52c555075402.jpg)
![Sem título7](https://user-images.githubusercontent.com/91357497/222984044-868949ff-5eea-4a95-bf2b-ad04f40f5847.jpg)
![Sem título8](https://user-images.githubusercontent.com/91357497/222984047-c1d6171c-3094-4358-9878-cf2f46ddbb3f.jpg)
![Sem título9](https://user-images.githubusercontent.com/91357497/222984048-f8edc69a-e0f9-4e31-8299-6f0062efd15a.jpg)
![Sem título10](https://user-images.githubusercontent.com/91357497/222984049-5b396da2-215f-495a-b10e-ace24baf5629.jpg)

