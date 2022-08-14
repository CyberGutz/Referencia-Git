# Referência Git

## Primeiros Passos
<br>

- Antes de tudo precisamos ter o git instalado na nossa máquina, se não o tiver, visite <a href = "https://git-scm.com/downloads">este link</a>.
- Após instalado, usaremos o comando `git --version` para verificar a versão da nossa instalação, bem como se o git foi instalado corretamente.

<br>

## Iniciando o Repositório

<br>

***Com o Git instalado na nossa máquina, devemos agora iniciar o repositório que desejamos controlar a versao.***

1. Crie uma pasta pro repositório local
2. Siga um dos passos abaixo
   1. Abra o terminal git da pasta com ***botão direito do mouse>git bash here*** (windows only).
   2. Abra o terminal git, e dê o comando `cd` até a pasta desejada.
   3. Se estiver no vscode, abra um novo terminal `Ctrl+Shift+'`.
3. Use o comando `git init` para iniciar o repositório.
4. ***Opcional:*** O nome das branches principais dos projetos vêm passando por um processo de transição, de *master* pra *main* (por motivos óbvios), se quiser mudar o nome da sua branch principal, utilize o comando: `git branch -M "main"`.

<br>

***Pronto! Temos o nosso repositório iniciado em nossa máquina.***

<br>

> NOTA: Ao iniciar o Repositório você notará que o indicativo da pasta terá um *(master)* ao lado, isso significa que você está na branch master do seu repositório, ou seja a branch principal.

<br>

## Linkando o Projeto ao GitHub

<br>

***Após criarmos nosso repositório, devemos linká-lo ao repositório do projeto que foi criado no GitHub, para isso, utilizaremos um comando simples:***

<br>

> `git remote add origin link_do_repositório`

<br>

***Esse comando basicamente diz ao github que queremos conectar o repositório remoto do github com o da nossa máquina e que queremos chamá-lo de "origin", que é um nome de uso comum para o repositório remoto, porém não obrigatório.***

<br>

## add, status, commit e push

<br>

***Após fazermos as preparações básicas do nosso projeto, podemos as adições e mudanças que desejamos ao nosso projeto. Após o termino da versão, devemos avisar o git que acabamos e que estamos mandar nossas alterações para o repositório remoto, para isso utilizaremos 2 comandos: add e commit.***

<br>

### Add:

O comando add tem 2 versões:

- `git add .` que é quando se quer mandar para o **staging** tudo o que foi modificado, adicionado ou apagado.
- `git add nomeDoArquivo` que é quando se quer atualizar um arquivo específico.
  

> **Staging** é a preparação para o commit, ou seja, você avisa o git o que você quer que saia naquela versão.

<br>

### Status:

Status é um comando para mostrar no terminal o estado do staging, ou seja, o que tem que ser commitado, o que foi alterado, adicionado ou removido.

- `git status`

<br> 

### Commit:
Quando já estamos contentes com as alterações que fizemos em nosso projeto, devemos criar nosso **commit**, que é quando se cria um nó na linha do tempo do projeto, ou seja, uma nova versão. Para isso usamos o seguinte comando: 

- `git commit -m "mensagem do commit"`

A mensagem do commit é o nome do commit, use-a para informar as mudanças que foram implementadas nesse commit **DE FORMA SUCINTA**. É importante fazer um resumo de suas alterações no projeto, não só para informar os colaboradores e utilizadores do projeto o que foi ou não alterado naquela versão.

<br>

*Faça commits de acordo com cada mudança que você implementar num projeto, para não ter que fazer um commit muito grande que mude o projeto em vários pontos. É importante fazer isso, pois qualquer coisa que dê erro no projeto, é possível restaurá-lo a commits antigos. Isso também previne mensagens de commits muito grandes e confusas.*

<br>

### Push:

Push é mandarmos nosso commit ao repositório remoto, realizando a alteração do nosso commit.

- `git push -u origin main` comando que só deve ser usado quando estamos fazendo nosso primeiro push. Ele reconhece nosso repositório remoto e confirma a ligação que fizemos do repositório em nossa máquina com o repositório remoto. (Nota do Autor: Explicação incerta. Se cometi um erro, me avise, ou sinta-se livre para propor uma alteração).
- `git push origin main` comando que puxa todas as branches para a main.
- `git push origin branch` comando que puxa as alterações somente para uma branch específica.

<br>

## Branch e Merge

<br>

### Branch

***Branches são ramificações do nosso projeto, use uma branch quando quer fazer uma alteração da qual não tem certeza de que vai implementá-la ou quando quer implementar uma feature que ainda está em fase de testes antes de uní-la à branch principal (main).***

Para criar uma branch, sair da branch atual e entrar na nova, use o comando:

- `git checkout -b "novaBranch"`

Para apenas criar uma nova branch, sem sair da sua branch atual, use o comando:

- `git branch "novaBranch"`

Para alternar para uma branch já existente, use o comando: 

- `git checkout nomeDaBranch`

<br>

### Merge

Merge é quando queremos juntar uma branch na branch principal (main ou master). Para isso, use o comando: 

- `git merge nomeDaBranch`
  
Para finalizar, dê um push na branch principal.

<br>

## Utilização e Colaboração:  Clone, Fork, Pull e Pull Request

<br>

### Clone
Clone é quando queremos utilizar um projeto já criado, clonando os seus arquivos para a nossa máquina. Para isso, use o seguinte comando:

- `git clone linkDoRepositório`

### Fork
Fork é quando copiamos um projeto para nosso próprio usuário do GitHub, seja para estudar o projeto, fazer nossas próprias alterações, ou apenas salvar o projeto com intuito de reaproveitar códigos ou features. Esse processo é feito no próprio GitHub, sem a necessidade de usar um comando.

### Pull

O pull é usado para atualizar um projeto que você tem clonado na sua máquina ou para implementar uma alteração que um colaborador fez em seu projeto.

- `git pull nomeDoProjeto`

### Pull Request
Quando você quer contribuir com algum projeto, você deve fazer o Pull Request no projeto original, de modo que o dono do projeto consegue revisar as suas alterações e decidir se vai implementá-las ou não. Este processo é feito na plataforma do GitHub.

<br>

> *Boas práticas de Pull Request: Quando fizer Pull Request, sempre deixe uma descrição das alterações que foram feitas, de modo que fique mais fácil para o dono do projeto revisá-las e menos confuso ou difícil de achar a sua alteração.*

<br>

## Epílogo

***Este guia de git foi feito com a ajuda dos vídeos Git e GitHub <a href = "https://youtu.be/DqTITcMq68k">Parte 1</a> e <a href = "https://youtu.be/UBAX-13g8OM">Parte 2</a> da Rafaella Ballerini, além de takes pessoais e comentários acerca do assunto. Sinta se livre para colaborar com este projeto e adicionar créditos no Epílogo. Espero que o guia seja de ajuda para outros estudantes que como eu, foram  uma vez confusos a respeito dessa tecnologia tão importante pro dia a dia de um programador.***