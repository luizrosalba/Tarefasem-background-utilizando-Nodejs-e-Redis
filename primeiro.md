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
- posso acompanhar os containers criados pelo comando : 
docker ps
