<p align="center">
 <img width="100px" src="https://res.cloudinary.com/teepublic/image/private/s--3G28Z3Jo--/t_Resized%20Artwork/c_fit,g_north_west,h_954,w_954/co_42332c,e_outline:35/co_42332c,e_outline:inner_fill:35/co_ffffff,e_outline:35/co_ffffff,e_outline:inner_fill:35/co_bbbbbb,e_outline:3:1000/c_mpad,g_center,h_1260,w_1260/b_rgb:eeeeee/c_limit,f_auto,h_630,q_90,w_630/v1589988736/production/designs/10390341_0.jpg" align="center" alt="GitHub Readme Stats" />
 <h2 align="center">Git Definitive ✅</h2>
 <p align="center">Projeto Desenvolvido para consulta de informações sobre o Git</p>
</p>

<br>

## Features

-   [Comandos Git](#comandos-git)
-   [Aliases](#aliases)
-   [Tags](#tags)
-   [Descartando Alterações](#descartando-alterações)

### **Principais Objetivos do Git:** 

>  Controle de Histórico
>
>  Trabalho em Equipe

---

### **Oque é o Git** 

>  É um sistema de controle de versões distribuído, usado para registrar o histórico de ediçoes de qualquer tipo de arquivo, usado principalmente em desenvolvimento de software. 

---

### **Plataformas de Hospedagens:** 

>  GitHub
>
>  Bitbucket


---

### **Comandos Git** 



    git init

>   Serve para criar um repositório LOCAL em algum diretório.

---

    git remote add origin <URL REMOTE REPOSITORY>

>   Serve para conectar um repositório local com o repositório remoto

---

    git remote get-url origin

>   Devolve a URL do repositório remoto no terminal

---

    git remote set-url origin <URL>

>  Serve para alterar a origem remota usando URL HTTPS, como por exemplo:

    git remote set-url origin https://devliborio:<app-password>@bitbucket.org/devliborio/git-test-repo.git

    git remote set-url origin <https://<username>:<app-password>@bitbucket.org/<username>/git-test-repo.git> -> (ESTRUTURA)

---

    git config --global user.name “username“

>  Para adicionar a configuração a todos os repositórios do seu usuário corrente do sistema operacional execute:

---

    git config --global user.email “e-mail“

>  Para adicionar a configuração a todos os repositórios do seu usuário corrente do sistema operacional execute:

---

    git config --local user.name “username“

>  Para adicionar a configuração a um repositório local específico, acesse o repositório e execute:

---

    git config --local user.email “email“

>  Para adicionar a configuração a um repositório local específico, acesse o repositório e execute:

---

    git config --system user.name "username"

>  Para adicionar a configuração a todos os repositórios de todos os usuários do sistema operacional execute:

---

    git config --systema user.email "email"

>  Para adicionar a configuração a todos os repositórios de todos os usuários do sistema operacional execute:

---

    git <verb> --help ou git <verb> -help

>  Serve para te retornar uma documentação do comando que você está com duvida, você coloca o nome do comando no lugar do `<verb>` e escolhe entre a versão 1 com o `--help` para te redirecionar para um site na web com a documentação ou a opção 2 -help que irá te retornar essa mesma documentação só que dessa vez no próprio  terminal.

---

    git add . 

    git add <nomedoarquivo>

> Ambos servem para adicionar o arquivo no status de preparo (staged), esse comando é obrigatório para que você consiga realizar o commit.
>
> Apesar dos dois comandos acima terem o mesmo objetivo em comum, os dois também tem diferenças, sendo o 1 acompanhado pelo “ . “ que serve para adicionar TODOS os arquivos de uma vez só para o status (staged), já o 2 exemplo serve para adicionar no status staged somente o arquivo que foi inserido no campo.

---

    git commit -m "<sua mensagem>"

> Após o arquivo ser movido para o status de staged ele está pronto para ser commitado, contudo é só usar este comando acompanhado pela mensagem referente a alteração que foi feita.

---

    git push -u origin master

    git push

> Após ter aplicado o commit você deve querer enviar para a sua plataforma de hospedagem seja o Bitbucket ou o GitHub por exemplo, para isso basta criar uma branch de rastreamento usando o primeiro comando (OBS: só precisa usar essa primeira opção caso seja sua primeira vez fazendo o processo e ainda não tenha uma branch de rastreamento.), caso você já tenha feito isso, basta usar o git push que ele irá enviar seu commit para a plataforma de hospedagem sem problema.

---

    git show

>  Para visualizar as alterações envolvidas em um determinado commit

---

    git status

>  Para visualizar o status do arquivo, sobre isso temos alguns tópicos importantes, vamos lá:
>
> novoarquivo →  status untracked = estado de arquivo não rastreado pelo git (não versionado pelo git)
>
> nesse caso você usa o `git add .` ou o `git add nomedoarquvio` para envia-lo para a área de preparo, dessa forma o status dele vai para →  staged
>
> Após o arquivo ser direcionado ao status de staged (preparo) ao você aplicar o comando commit ele começa a ser versionado pelo git e passa a ter o estado →  unmodified
>
> Caso você edite este arquivo ele irá para o status →  modified
>
> Para aplicar as alterações e deixar ele novamente preparado para o commit, basta você enviar ele novamente para o status staged usando o `git add .` ou `git add nomedoarquivo`

---

Git hash order:

`hash commit → hash tree → hash blobs → conteudo do arquivo.`

---

    git cat-file -t <pedaço do hash>

> Serve para mostrar o tipo da chave hash que estamos querendo saber.

---

    git cat-file -p <pedaço do hash>

> Serve para mostrar o conteúdo da chave hash pode ser uma tree, blobs.

---

    git checkout -b <branch>

> Esse comando cria uma nova branch e altera a referência HEAD para a mesma, tornando-a branch corrente.
>
> Porém há outras formas de criar uma branch, sem necessariamente alternar para a recém criada. Para criar uma nova branch a partir da branch corrente, você pode utilizar o comando:

    git branch <nome da nova branch>

> Para criar uma nova branch a partir de uma branch especifica utilize o comando

    git branch -c <nome da branch específica> <nome da nova branch>

---

    git branch -a

> Ele irá listar todas as nossas branch, tanto as locais que vão estar em branco quanto as de rastreamento que iram estar em vermelho.
>
> E sendo a branch verde com asterisco a nossa branch corrente (branch atual)

---

    git branch -m "change username"

> Serve para alterar o nome da branch

---

### **Aliases** 

> São usados para criar comandos menores que correspondem a comandos maiores, como segue no exemplo abaixo:

    git config --global alias.hist 'log --pretty=format:"%h %ad | %s%d [%an]" --graph --date=short

> Nesse exemplo nosso criamos um alias para acessar o Git log, especificando um pouco o que vamos ter de saída do comando, vamos entender o que é cada estrutura deste comando:

`%h`  = Hash do commit abreviado

`%ad` = Data do commit

`%s` = comentário

`%d` = Decorações do commit (Ex: head de branches, logs)

`%an` = Autor do commit

---

### **Tags**  

> Etiquetas ou Tags geralmente são usadas para marcar lançamentos estáveis ou a conquistas de marcos importantes
>
> Podem ajudar os usuário de repositório a navegar facilmente para as partes importantes do historio de códigos, como pontos de liberação.
>
> As Tags podem ser divididas em dois grupos as Tags Leves e as Tags Anotadas, irei explicar abaixo as diferenças:
>
> **Tags Leves** → Mais apropriadas para o uso privado ou temporário, você pode definir uma tag em algum commit usando essa estrutura `git tag <'nome da tag'>` e para Deletar uma tag temporária é só realizar o seguinte comando `git tag -d <'nome da tag'>` .
>
> **Tags Anotadas** →  São aquelas que devem ser publicadas para outros contribuidores, provavelmente novas versões, você pode definir essa tag usando a seguinte estrutura  `git tag -a <"titulo da tag"> -m <descrição da tag>`
> 
> Até o momento só acrescentamos a Tag ao repositório local.
>
> Agora como empurramos uma Tag para um repositório remoto?
>
> Primeiramente precisamos entender o seguinte, o git push por si próprio não envia Tags para o repositório remoto, então para solucionar isso podemos usar a seguinte estrutura `git push --tags` que irá enviar por exemplo uma nova tag.
> 
> Entretanto você precisara fazer dois pushs diferentes toda vez que tiver um commit para ser enviado e uma tag, porque não fazer tudo junto logo, não seria MUITO melhor ?
>
> Pois bem, temos como configurar isso fazendo o seguinte:
>
> Para adicionar a configuração a um repositório local específico, acesse o repositório e execute:

    git config --local push.followTags true

> Para adicionar a configuração a todos os repositórios do seu usuário corrente do sistema operacional execute:

    git config --global push.followTags true

> Para adicionar a configuração a todos os repositórios de todos os usuários do sistema operacional execute:

    git config --system push.followTags true

---    

### **Descartando Alterações** 

<br>

  #### **Descartando mudanças Locais**

> Fazendo com arquivo já criado

    echo "conteudo do arquivo" > arquivo.txt

    git status

    git restore arquivo.txt -> Ele restaura as alterações

    git status

> Fazendo com arquivo novo

    touch arquivonovo.txt

    git status

> tente utilizar `git restore arquivonovo.txt` este comando não terá efeito pois o novo arquivo não é rastreado pelo git (untracked)
>
> Para descartar neste caso utilize `git clean arquivonovo.txt -f` detalhe que o parâmetro `-f`  significa force a limpeza(exclusão) desse arquivo
>
> Para remover todos os arquivos que não são rastreados use `git clean -f`
>
> Agora caso você queira verificar primeiro todos os arquivos não rastreados antes de limpa-los execute: `git clean -n` e depois use `git clean -f`
<br>

---

 #### **Descartando mudanças do Stage**


    echo "conteudo do arquivo" > arquivo.txt

    touch arquivonovo.txt

    git status

    git add .

    git restore --staged →  Para remover o status de staged e retornar ao status corrente

    git status  → Note que ambos os arquivos que foram enviados para o status staged voltaram ao padrão.
    
---

 #### **Observação:** 
 
 > Além de desfazer alterações, o comando restore também pode ser utilizado para restaurar versões anteriores em um arquivo.
 >
 > Para isso, você pode utilizar o seguinte comando:

    git restore --source <hash do commit> <nome do arquivo> 

---

 #### **Revert commit**

> Vamos criar um arquivo novo:

    touch arquivonovo.txt

> Agora vamos inserir um conteudo dentro deste arquivo:

    echo "conteudo do arquivo novo" > arquivonovo.txt

> Vamos adicionar ele no status de "Staged" usando o comando abaixo:

    git add .

> Agora é só fazer o commit:

    git commit -m "novo arquivo arquivonovo.txt"

> Agora vamos desfazer esse ultimo commit usando esse comando:

    git revert HEAD --no-edit

> o parâmetro `--no-edit` fará com que o GIT não abra o editor de texto padrão.
>
> o git revert pode receber um id de commit ou qualquer refêrencia tag, branch ou HEAD, no caso acima foi revertido o commit corrente. Para reverter o penúltimo commit pode-se utilizar `git revert HEAD~1`

---
### **Reset Commit**

> O comando git reset é uma ferramenta mais versátil e um mais complexa que o revert, sendo classificada por três tipos: **soft** | **mixed** | **hard**.
>
> Se nenhum dos três parâmetros forem definidos o GIT assume como padrão o **mixed**

<br>

> Agora vamos entender melhor como funciona o **Reset Commit - SOFT**
> 
> Vamos adicionar um novo arquivo chamado `soft.txt`

    touch soft.txt

    git add soft.txt

    git commit -m 'adding soft test'

    git hist

    git reset --soft head~
    
    git hist

    git status

> O parametro soft ele remove o commit e preserva a área de trabalho, deixando o arquivo no status de staged, se caso for da nossa preferencia limpar tbm a área de trabalho usando o parâmetro soft, vamos ter que usar o git restore desse jeito: `git restore --staged soft.txt` e depois `git clean soft.txt -f`
