Kenzie API - Fake-API

Esta é uma aplicação simples desenvolvida pro mim. 

“Sempre passar o que você aprendeu. - Mestre Yoda”

Endpoints

A aplicação contém de 3 EndPoints, podendo cadastrar Usuários e amigos Imaginarios para compartilhar com todos.

URL:  https://jason-server-atividade.herokuapp.com

Rotas que não precisam de autenticação

Nessa aplicação é possivel visualizar todos os amigos Imaginários cadastrados.

GET /amigoImaginario


Nessa aplicação é possível cadastrar usuários para interaragir com API.Apenas E-mail e senha são necessários é claro, então sinta-se livre para adicionar novas prodrpiedades:

POST /register

    {
	    "email": "Robin@gmail.com",
	    "password": "nicor0bin*",
	    "name": "Nico Robin",
	    "age": "28"
    }


Nessa aplicação é possivél Criar um amigo imaginario após, estar logado, é claro.  O token é gerado quando o Usuário é Cadastrado.

Rotas que precisam de autenticação

POST /amigoImaginario
    {
        title: title,
        status: status,
    },
    {
        headers: 
            {
                 Authorization: `Bearer ${token}`
            }
    }

GET /users/:id

Nessa Aplicação é possivel trazer os dados dos usuários.

    {
        headers: 
            {
                 Authorization: `Bearer ${token}`
            }
    }
