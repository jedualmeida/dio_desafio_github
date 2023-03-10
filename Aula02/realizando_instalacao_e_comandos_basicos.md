# Instalação do Git no Windows

1. Acesse o [site oficial do Git](https://git-scm.com/downloads) na página de downloads e clique em **"Download for Windows"**;
2. Após o instalador ser baixado, execute-o como administrador;
3. Nas janelas que se sucedem, clique em **"Next"** e por fim em **"Install"**;
4. Para concluir o processo de instalação clique em **"Finish"**.



# Principais comandos do Git

 Utilize o terminal **Git Bash** para executar os comandos via CLI. Este é o aplicativo para ambientes de sistema operacional Windows que oferece a camada de emulação para a experiência em linha de comando Git. **"Bash"** é acrônico para **"Bourne Again Shell"**. ***Shells*** são aplicativos  terminais usados como interface em sistemas operacionais por meio de  comandos gravados.

### git config

A primeira coisa que você deve fazer quando instalar o Git é definir o seu nome de usuário e endereço de e-mail. Isso é importante porque  todos os commits no Git utilizam essas informações, e está imutavelmente anexado nos commits que você realiza:

*Obs: utilize o mesmo **username** e **e-mail** cadastrado no Github*!

git config --global user.name "Seu.Nome"                                            
git config --global user.email seu.email@example.com.br                                     

### git help

Se você precisar de ajuda ao usar Git, existem três maneiras de obter a ajuda para qualquer um dos comandos Git:

git help {comando}                                            
git {comando} --help                                            
man git- {comando}                                        

### git init

Caso você esteja iniciando o monitoramento de um projeto existente com Git, você precisa ir para o diretório do projeto e digitar:

git init

Isso cria um novo subdiretório oculto chamado **.git** que contem todos os arquivos necessários do seu repositório. Neste ponto, nada em seu projeto é monitorado.

### git clone

Você clona um repositório público existente no Github, basta copiar a **URL HTTPS** do diretório e digitar o comando:

git clone <link https do repositorio a ser clonado>

### git status

A principal ferramenta utilizada para determinar quais arquivos estão em quais estados é o comando:                                        

git status

O comando lhe mostra em qual ***branch*** você se encontra e os estados em que os arquivos e pastas do repositório estão.

### git commit

Armazena o conteúdo atual do índice em um novo commit, juntamente com uma mensagem de registro do usuário que descreve as mudanças.                                            
Se usa o commit depois de já ter feito o **git add**, para fazer o commit:

git commit -m "Mensagem"

Para commitar também os arquivos versionados mesmo não estando no Stage basta adicionar o parâmetro -a

git commit **-a** -m "Mensagem"

### git push

**O git push** é o comando em que você transfere commits a partir do seu repositório local para um repositório remoto. É a contrapartida do **git fetch**, que busca importações e comprometem as agências locais, utilizando o **git push** as exportações comprometem as filiais remotas. Para fazer isso, você executa **git push [nome_do_repositório_remoto] [nome_da_sua_branch_local]**, que vai tentar fazer que o **[nome_do_repositório_remoto]** receba a sua branch **[nome_da_sua_branch_local]** contendo todos seus commits com alterações. Por exemplo:

git push origin master