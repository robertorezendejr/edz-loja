### Startando a loja
npm run dev -- -p 5000

#### A Loja é a:
609f2face5060f034cf1725c

Antigas
609f27698b28638646f158e0

609ee1bea70dad7a34e89151

### Para rodar a aplicação na pasta API
nodemon
###### ou
npm run dev

### API local host
http://localhost:3000/

### dashboard
http://localhost:5000/
### Loja
http://localhost:8000/

## MongoDB
##### startar Mongodb dentro da pasta bin
./mongod --dbpath=../../data/db/
#### startar o mongo
dentro da pasta bin rodar:
open mongo




Inserindo no MongoDB

Se você rodar dentro do terminal do MongoDB, o comando:

db.clientes.findOne({"usuario":ObjectId("60a032ac4a1a9617f4ca35fb")}); /*<-- ID do usuário "roberto@email.com"*/

O que ele retorna? Se ele retornar vazio, aí quer dizer que realmente não tem o cliente para esse usuário, e esse é o erro.

Aí para corrigir ele, você vai precisar criar um cliente para ele. Como o processo de criação de um cliente usando a API cria o usuário junto, nesse caso você precisa criar ele manualmente, usando o terminal do MongoDB mesmo. 

Você pode fazer isso usando o comando:

db.clientes.insert({
    "usuario": ObjectId("60a032ac4a1a9617f4ca35fb"), /*<-- ID do usuário "roberto@email.com"*/
    "nome": "Nome",
    "dataDeNascimento": "1990-01-01",
    "cpf": "111.111.111-11",
    "telefones": ["(11) 1111-1111"],
    "loja": ObjectId("709f27698b28638646f158e0"), /*<-- ID da loja*/
    "endereco": {
        "local": "Rua teste",
        "numero": "123",
        "complemento": "casa",
        "bairro": "centro",
        "cidade": "teste",
        "estado": "SP",
        "CEP": "01000-100"
    }
});

Fazendo isso acredito que já vai funcionar tudo certo.

Fico a disposição!

Atenciosamente,
- Mateus Machado.