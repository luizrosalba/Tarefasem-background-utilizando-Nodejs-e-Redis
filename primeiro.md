# Atividades deste Labs 

- Instalei o docker https://hub.docker.com/

-  Docker é uma plataforma de código aberto, desenvolvido na linguagem Go e criada pelo próprio Google. 
Por ser de alto desempenho, o software garante maior facilidade na criação e administração de ambientes isolados, 
garantindo a rápida disponibilização de programas para o usuário final.

- O Docker tem como objetivo criar, testar e implementar aplicações em um ambiente separado da máquina original,
chamado de container. Dessa forma, o desenvolvedor consegue empacotar o software de maneira padronizada. 
Isso ocorre porque a plataforma disponibiliza funções básicas para sua execução,
como: código, bibliotecas, runtime e ferramentas do sistema.

Um arquivo Docker pode ser formado por diversas camadas diferentes, onde se dividem em dois grupos:

- Imagens: elas são formadas por diferentes camadas. Com a sua utilização, o usuário pode facilmente compartilhar 
um aplicativo ou um conjunto de serviços em diversos ambientes. Quando há alguma alteração na imagem, 
ou uso de um comando como executar ou copiar, é criada uma camada.

-Containers: são formadas na reutilização das camadas. Um container é o local onde estão as modificações da
aplicação que está em execução. É por meio dele que o usuário pode modificar uma imagem.

- Permite Reversão

- permite Implantação rápida

- criei uma conta 

- realizei o tutorial de instalação od docker desktop para windows gerando assim um container docker -tutorial rodando na porta 80 

-  não consegui startar o container do tutorial (ocorreu algum erro de portas ... ) 

- Para o Labs vou precisar do redis , para criar este container executei : 
docker run --name redis -p 6379:6379 -d -t redis:alpine
- Ele usou a imagem padrão do  Linux 687e7ed93cd5 4.19.76-linuxkit #1 SMP Tue May 26 11:42:35 UTC 2020 x86_64 Linux
- agora pelo docker desktop eu tenho acesso a esta máquina virtual :D 
posso acompanhar os containers criados pelo comando : 
- docker ps

 insatlei o yarn 
- apk add yarn
- yarn --version

- usar o Visual Studio Code com o container : 
- adicionar a extensao do docker 
- adicionar a extensão do remote container 
- criar a paste : 
- no VS F1 
- remote containers : attach to running container 

- está pronto para usar ! 

- criei uma pasta em ~/.vscoder-server/teste2
Instalei o yarn express nodemailer dotenv
- yarn add express nodemailer dotenv
Instalei o gitignore no container para subir o codigo para o git 
- busquei o pacote gitignore , já me deu a opção de instalar no container e instalei com um clique 
- abri a pasta teste2 

- adicionei o git no container 
RUN apk update && apk upgrade && apk add --no-cache bash git openssh
- fui pra pasta teste2 e adicionei o controle git 
- yarn add git 
- Ele já atualizou as dependencias do projeto no json com o git 
```Javascript
{
  "dependencies": {
    "dotenv": "^8.2.0",
    "express": "^4.17.1",
    "git": "^0.1.5",
    "nodemailer": "^6.4.11"
  }
}
```
- dentro da pasta2 git init 
Initialized empty Git repository in /root/.vscode-server/teste2/.git/
criei um arquivo .gitignore com a seguinte linha : node_modules
- isso faz com que o git ignore os modulos do node na hora de fazer os meus commits
- Adicionei o nodemon no projeto 
yarn add nodemon sucrase -D
-Criei o arquivo nodemon.json dentre de teste2 
criei a pasta src e dentro dela coloquei servers.js 
- import 'dotenv/config';
dotenv permite usar variaveis de ambiente 
- Criei o arquivo .env na pasta teste 2 e coloquei a o comando : PORT=8080
.env é bom para usar com variaveis imutaveis como credeciasi de acesso , servidor etc... 
- editei e meu server.js ficou assim : 
```Javascript 

import 'dotenv/config';
import express from 'express'; 

const app = express();

app.arguments(express.json());

app.listen(process.env.PORT, () => {
    console.log(`Server running on the ${process.env.PORT}`)
});

```

const app = express();










