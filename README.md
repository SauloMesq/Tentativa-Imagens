
![M@IN](https://github.com/SauloMesq/Tentativa-Imagens/assets/136653514/0b380a0f-674a-40ed-97be-022c73c907fb)

M@IN - CONEXÃO COM O ESSENCIAL!
M@IN é uma aplicação que permite o envio de e-mails automatizados a usuários cadastrados em um banco de dados;


Com o programa é possível criar, buscar, deletar e atulaizar o cadastro de usuários, associando-os a endereços eletrônicos e um id, como também a uma empresa ou organização;

Há também um repositório de mensagens que pode receber temas específios para elas, o qual também é possível gerenciar de forma constante, fazendo busca por assuntos e registro(usuário, id e listar por empesa;

Utilizando uma ferramenta auxiliar (Postman), é possível confirmar o envio, retornando data e horário. O aplicativo roda em nuvem graças ao Heroku, plataforma de Deploy. Desta forma, é possível acessar as funções em qualquer máquina.

Criado por
Basílio Queiroz
Fábio Lins
José Gabriel Oliveira
Saulo Mesquita


Mentoria:

Ana Beatriz Cavalcanti

Trabalho de conclusão do curso NExT - Nova Experiência de Trabalho; 
OBS: Sem fins comerciais;

O que você vai precisar para rodar locamente a aplicação
- OpenJDK 17.0.2 +;
- Maven 3.9.4 +;
- Uma ferramenta para fazer REST requests. (Ex: Postman, Insonia);
- Spring Boot 3.1.3 +;
- JBDC Connector.
OBS: Você pode copiar o código direto para sua IDE. Nós usamos o VS Code;


CRUD de Usuários
Caso que queira rodar a aplicação localmente, primeiro você terá que ir em Aplication Properties e atualizar os dados de username e senha, considerando seu banco de dados local de sua preferência (JBDC Connector) e o endereço que enviará as mensagens pré-formatadas;

Depois de rodar a aplicação e com o banco de dados sincronizado na sua máquina, você precisará de uma ferramenta para fazer REST Requests. Todos os testes de funcionalidade do CRUD e do envio de e-mail deste projeto foram feitos usando o Postman.

O banco de dados recebe informações sobre usuários, com os parâmetros "name", "email" e "organization".

Utilize o seguinte formato:

{
"name": "JoãoMaria",
"email": "joaomaria@gmail.com"
"organization": "cesar"
}


http://localhost:8080/user - Para uso local

////
https://api-yara-sendingemail.herokuapp.com/users - Para uso em nuvem Usando essa URL request no Postman, você pode utilizar os seguintes métodos: POST, para cadastrar usuários (recomendamos não colocar espaços em branco); GET, para listar todos usuários cadastrados;
////

http://localhost:8080/users/id - Para uso local

////
https://api-yara-sendingemail.herokuapp.com/users/id - Para uso em nuvem Colocando o número do ID do usuário no lugar do "id", você pode usar os seguintes métodos: GET, para buscar o usuário por ID; DELETE, para apagar o usuário identificado pelo ID; PUT, para atualizar dados do usuário identificado pelo ID.
////

exemplos: http://localhost:8080/users/12 - Para uso local

////
[https://api-yara-sendingemail.herokuapp.com/users/12] (https://api-yara-sendingemail.herokuapp.com/users/12) - Para uso em nuvem
////


CRUD de Mensagens
Há também uma forma de adicionar mensagens pré-formatadas na tabela, com os parâmetros "Subject" e "Text".

Utilize o seguinte formato:

{
"Subject": "Parabéns!",
"Text": "Feliz aniversário !!!"
}

http://localhost:8080/message - Para uso local

////
https://api-yara-sendingemail.herokuapp.com/message - Para uso em nuvem Usando essa URL request no Postman, você pode utilizar os seguintes métodos: POST, para cadastrar mensagens; GET, para listar todas mensagens cadastradas;
////

http://localhost:8080/message/id - Para uso local

https://api-yara-sendingemail.herokuapp.com/message - Para uso em nuvem Colocando o número do ID do usuário depois do "id", você pode usar os seguintes métodos: GET, para buscar a mensagem por ID; DELETE, para apagar a mensagem identificado pelo ID; PUT, para atualizar dados da mensagem identificado pelo ID.
Enviando e-mails
Para enviar e-mails utilizando a tabela de usuários, você deve seguir o seguintes modelos:

http://localhost:8080/sending-email/nameUser - Para uso local

https://api-yara-sendingemail.herokuapp.com/sending-email/nameUser - Para uso em nuvem Para mandar o e-mail para um usuário cadastrado no banco de dados, troque "nameUser" pelo nome do usuário que você quer enviar.
Exemplo: sending-email/AllanArruda

No corpo do email, você deve preencher os campos subject e text;

Utilize o seguinte formato:

{

"subject": "Aniversário",

"text": "Parabéns João !!"

}

Para enviar e-mail usando mensagens pré-cadastradas para usuários cadastrados, utilize a seguinte URL: http://localhost:8080/sending-email/nameUser/messageSubject - Para uso local

https://api-yara-sendingemail.herokuapp.com/sending-email/nameUser/messageSubject - Para uso em nuvem
No campo "nameUser" será passado o nome conforme foi cadastrado, sem espaço, e no "messageSubject" será passado o assunto da mensagem de e-mail também conforme cadastrado no banco de dados:

exemplo: http://localhost:8080/sending-email/TulioAlbu/Aniversario - Para uso local

https://api-yara-sendingemail.herokuapp.com/sending-email/TulioAlbu/Aniversario - Para uso em nuvem


Nossos contatos:
Basílio Queiroz:

Github
Linkedin

Fábio Lins:

Github
Linkedin

José Gabriel Oliveira:

Github
Linkedin

Saulo Mesquita:

GitHub: https://github.com/SauloMesq
Linkedin
