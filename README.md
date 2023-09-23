
![M@IN](https://github.com/SauloMesq/Tentativa-Imagens/assets/136653514/0b380a0f-674a-40ed-97be-022c73c907fb)

<h1>M@IN - CONEXÃO COM O ESSENCIAL!</h1> 
<h2>M@IN é uma aplicação que permite o envio de e-mails automatizados a partir de cadastros de usuários em um banco de dados;</h2>


Com o programa é possível criar, buscar, deletar e atualizar o cadastro de usuários, associando-os a endereços eletrônicos e um id, como também a uma empresa ou organização;

Há também um repositório de mensagens que pode receber temas específios para elas, o qual também é possível gerenciar de forma constante, fazendo busca por assuntos e registro (usuário, id e listar por uma empresa ou organização da qual o usuário faça parte;
Com uma ferramenta auxiliar, é possível confirmar o envio, retornando data e horário.


### Criado por:
- Basílio Lima de Queiroz Santos;
- Fábio Lins de Oliveira;
- José Gabriel Coelho Oliveira;
- Saulo Mesquita


Mentoria:
#### Ana Beatriz Cavalcanti Ribeiro

- Linkedin: https://www.linkedin.com/in/anabeatrizcavalcantir/


#
# Trabalho de conclusão do curso NExT - Nova Experiência de Trabalho (sem fins comerciais)
#

### O que é necessário para executar a aplicação locamente:
```
- OpenJDK 17.0.2 +;
- Maven 3.9.4 +;
- Uma ferramenta auxiliar para fazer REST requests. (Ex: Postman, Insomnia);
- Spring Boot 3.1.3 +;
- Um concetor a banco de dados (JDBC) (JBDC Connector).
```
  
##### OBS: Você pode copiar o código direto para sua IDE.


## Funcionalidades (CRUD) - Usuários:
Para executar a aplicação localmente, com o código aberto na sua IDE, primeiro você deverá ir em Aplication Properties e atualizar os dados de usuário (username=) e senha (password=), considerando seu banco de dados local de sua preferência (JBDC Connector) e o endereço que enviará as mensagens pré-formatadas;

Depois de executar a aplicação e conectado ao banco de dados na sua máquina, você precisará de uma ferramenta para fazer REST Requests. Todos os testes de funcionalidade do CRUD e do envio de e-mail deste projeto foram feitos usando o Postman ou Insomnia.
O banco de dados recebe informações sobre usuários, com os parâmetros "name", "email" e "organization".

Na feramente para REST Request, utilize o seguinte formato:
```
{
"name": "JoãoMaria";
"email": "joaomaria@gmail.com";
"organization": "cesar";
"func": "Desenvolvedor";
}
```

http://localhost:8080/user - (uso local)
Usando essa e as outras URLs request no Postman ou Insomnia, você pode utilizar os seguintes métodos: 
- *POST*, para cadastrar usuários;
- *GET*, para listar todos usuários cadastrados;

http://localhost:8080/users/id (uso local)

Colocando o número do ID do usuário no lugar do "id", você pode usar os seguintes métodos: *GET*, para buscar o usuário por ID; *DELETE*, para apagar o usuário identificado pelo ID; *PUT*, para atualizar dados do usuário identificado pelo ID.
É possível atualizar o usuário modificando os atributos do mesmo: “email”, “name”, “organization” e “func”.
- EX: http://localhost:8080/users/3592347



#
## Funcionalidades (CRUD) - Mensagens:
Há também uma forma de adicionar mensagens pré-formatadas na tabela, com os parâmetros "Subject" e "Text".

Na feramenta para REST Request, utilize o seguinte formato:
```
{
"Subject": "Infrome de planejamento";
"Text": "Execução do panejamento confirmada.";
}
```

http://localhost:8080/message - (uso local)
Usando essa URL request no ferramente de REST request, você pode utilizar os seguintes métodos: *POST*, para cadastrar mensagens; *GET*, para listar todas mensagens cadastradas;



http://localhost:8080/message/id - (uso local)
Colocando o número do ID do usuário depois do "id", você pode usar os seguintes métodos: *GET*, para buscar a mensagem por ID; *DELETE*, para apagar a mensagem identificado pelo ID; *PUT*, para atualizar dados da mensagem identificado pelo ID.




## Enviando e-mails:
Para enviar e-mails utilizando a tabela de usuários, você deve seguir o seguintes modelos:

- http://localhost:8080/  - (uso local)
Para mandar o e-mail para um usuário cadastrado no banco de dados, troque "user" pelo nome do usuário que você quer enviar.


No corpo do email, você deve preencher os campos "subject" e "text";

Utilize o seguinte formato:
```
{
"subject": "Aniversário",
"text": "Parabéns, João !!"
}
```


## Para enviar e-mail usando mensagens pré-cadastradas para usuários cadastrados, utilize a seguinte URL:

- http://localhost:8080/    - (uso local)

No campo "user" será passado o nome conforme foi cadastrado, sem espaço, e no "subject" será passado o assunto da mensagem de e-mail também conforme cadastrado no banco de dados:

- http://localhost:8080/sending-email/JoaoMaria/ - (uso local)



##

## Nossos contatos:

| Basílio Queiroz: |
| ------ |
- Github: https://github.com/91basilio
- Linkedin: https://www.linkedin.com/in/basilioqueiroz/

| Fábio Lins: |
| ------ |
- Github: https://github.com/fllins
- Linkedin:

| José Gabriel Oliveira: |
| ------ |
- Github: https://github.com/Gabriel-Oliveira25
- Linkedin:

| Saulo Mesquita: |
| ------ |
- GitHub: https://github.com/SauloMesq
- Linkedin: https://www.linkedin.com/in/saulo-mesquita-09024a249/

![M@IN 2](https://github.com/SauloMesq/Tentativa-Imagens/assets/136653514/bcca71ba-bc23-43cb-bcae-d4894bc538f4)
