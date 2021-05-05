# Hey! 👤
[![Github Badge](https://img.shields.io/badge/-Github-000?style=flat-square&logo=Github&logoColor=white&link=https://github.com/luciolemos)](https://github.com/luciolemos)
[![Linkedin Badge](https://img.shields.io/badge/-LinkedIn-blue?style=flat-square&logo=Linkedin&logoColor=white&link=https://www.linkedin.com/in/lucio-lemos-a550441a1/)](https://www.linkedin.com/in/lucio-lemos-a550441a1/)
[![Twitter Badge](https://img.shields.io/badge/-Twitter-1ca0f1?style=flat-square&labelColor=1ca0f1&logo=twitter&logoColor=white&link=https://twitter.com/lucciolemos)](https://twitter.com/lucciolemos)
[![Youtube Badge](https://img.shields.io/badge/-YouTube-ff0000?style=flat-square&labelColor=ff0000&logo=youtube&logoColor=white&link=https://studio.youtube.com/channel/UCrNM1nr2nw0lSqMD10m6rLw)](#)
## Começando com o **EXPRESS** 📌: 
O [express](https://www.npmjs.com/package/express-generator) tem sua própria ferramenta de linha de comando, o `express-generator`, que facilita a inicialização de novos aplicativos. Use o gerador de aplicativos do express para criar rapidamente uma estrutura básica de aplicativo, seguindo os passos abaixo descritos.
### Resumo das rotinas que seráo executadas no _bash_:
- Instale o Node `$ sudo apt-get install nodejs`. O NPM é o Gerenciador de Pacotes do Node (Node Package Manager). Node e NPM são empacotados juntos.
- Instale o express com o comando `$ npm install express-generator -g`.
- Crie o diretório `my_app` da sua aplicação express com `$ express my_app -e --git`.
- Navegue para dentro de `my_app` com o comando `$ cd my_app`.
- Instale as dependências do Node, que o projeto necessita com `$ npm install`;  
- Verificando se há atividade na porta 3000 `$ sudo netstat -nlp | grep :3000`;
- Interrompendo o processo na porta 3000, caso haja `$ kill <PID>`; 
- Carregando o projeto no vscode com `$ code .`;
- Abrindo o terminal no vscode `Ctrl+J`;
- Startando a aplicação com `$ DEBUG=myapp:* npm start`. 
- Rodando a aplicação digitando no browser `http://localhost:3000`.

#### ✔️ Criando o projeto `my_app` com `$ express my_app -e --git`.
A flag `--git` cria na raís do projeto, o arquivo oculto `my_app/.gitignore`, que contém as diretivas de quais arquivos (ou padrões) o git deve ignorar. 


    luciolemos@dev:~/vscode$ express my_app -e --git

    warning: option `--ejs' has been renamed to `--view=ejs'


    create : my_app/
    create : my_app/public/
    create : my_app/public/javascripts/
    create : my_app/public/images/
    create : my_app/public/stylesheets/
    create : my_app/public/stylesheets/style.css
    create : my_app/routes/
    create : my_app/routes/index.js
    create : my_app/routes/users.js
    create : my_app/views/
    create : my_app/views/error.ejs
    create : my_app/views/index.ejs
    create : my_app/.gitignore
    create : my_app/app.js
    create : my_app/package.json
    create : my_app/bin/
    create : my_app/bin/www

    change directory:
        $ cd my_app

    install dependencies:
        $ npm install

    run the app:
        $ DEBUG=my-app:* npm start
#### ✔️ Navegando para dentro do projeto com `$ cd my_app`.
    luciolemos@dev:~/vscode$ cd my_app
#### ✔️ O bloco de código a seguir será gerado durante a criação do repositório remoto, copie e cole-o no terminal.


    echo "# my_app" >> README.md
    git init
    git add README.md
    git commit -m "first commit"
    git branch -M main
    git remote add origin https://github.com/luciolemos/my_app.git
    git push -u origin main

#### ✔️ Copie e cole no terminal, o bloco de código acima, gerado por ocasião da criação do repositório remoto, onde cada linha executada realiza:

#### ✔️ Cria o arquivo **README.md** `$ echo "# my_app" >> README.md`.
    luciolemos@dev:~/vscode/my_app$ echo "# my_app" >> README.md
#### ✔️ Inicia o projeto com `git init`.    
    luciolemos@dev:~/vscode/my_app$ git init
    Initialized empty Git repository in /home/luciolemos/vscode/my_app/.git/

#### ✔️ Adiciona o arquivo **README.md** ao repositório local com `git add README.md`. 
    luciolemos@dev:~/vscode/my_app$ git add README.md  

#### ✔️ Salva as alterações feitas no repositório local com `git commit -m "first commit"`.
    luciolemos@dev:~/vscode/my_app$ git commit -m "first commit"
    [master (root-commit) f1f005f] first commit
    1 file changed, 1 insertion(+)
    create mode 100644 README.md

#### ✔️ Informa o ramo do projeto onde serão salvas as alterações.
    luciolemos@dev:~/vscode/my_app$ git branch -M main

#### ✔️ Informa o camiho do repositório remoto
    luciolemos@dev:~/vscode/my_app$ git remote add origin https://github.com/luciolemos/my_app.git

#### ✔️ Empurra (_push_) as alterações para o repositório remoto
    luciolemos@dev:~/vscode/my_app$ git push -u origin main
    Username for 'https://github.com': luciolemos
    Password for 'https://luciolemos@github.com': 
    Enumerating objects: 3, done.
    Counting objects: 100% (3/3), done.
    Writing objects: 100% (3/3), 219 bytes | 219.00 KiB/s, done.
    Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
    To https://github.com/luciolemos/my_app.git
    * [new branch]      main -> main
    Branch 'main' set up to track remote branch 'main' from 'origin'.

#### ✔️ Instalando as dependências do Node no projeto criado com `$ npm install`. Repare que nesse momento é criado o diretório `node_modules`, na raís do projeto.


    luciolemos@dev:~/vscode/my_app$ npm install

    added 54 packages, and audited 55 packages in 5s

    found 0 vulnerabilities

### Identificando e parando o processo em execução na porta 3000, caso haja:
#### ✔️ Localizando o PID (Process ID) escutando na porta 3000 com `$ sudo netstat -nlp | grep :3000`:
    luciolemos@dev:~/vscode/my_app$ sudo netstat -nlp | grep :3000
    [sudo] senha para luciolemos:     
    tcp6       0      0 :::3000                 :::*                    OUÇA       11020/node 

#### ✔️ O ID do processo é o número antes do nome do processo na sexta coluna (11020). Pare o processo com o comando `$ kill 11020`.
    luciolemos@dev:~/vscode/my_app$ kill 11020
### Rodando nosso projeto
#### ✔️ Startando na porta 3000.
    luciolemos@dev:~/vscode/my_app$ DEBUG=my-app:* npm start

    > my-app@0.0.0 start
    > node ./bin/www

    my-app:server Listening on port 3000 +0ms

#### ✔️ Abrindo o diretório corrente no VSCode com `$ code .`: 
    luciolemos@dev:~/vscode/my_app$ code .
#### ✔️ Digitando no browser `http://localhost:3000`.