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
-   [Revert Commit](#revert-commit)
-   [Reset Commit](#reset-commit)
-   [Reflog](#reflog)
-   [Merge](#merge)
-   [Merge Three-Way](#merge-three-way)
-   [Merge No-fast-forward](#merge-no-fast-forward)
-   [Dag](#dag)
-   [Conflitos](#conflitos)
-   [Trabalho Colaborativo](#trabalho-colaborativo)
-   [Fetch](#fetch)
-   [Pull](#pull)
-   [Bloqueio de Push](#bloqueio-de-push)
-   [Rebase](#rebase)
-   [The Golden rule of rebase](#the-golden-rule-of-rebase)
-   [Merge x Rebase](#merge-x-rebase)
-   [Emendar Commit](#emendar-commit)
-   [Squash Merge](#squash-merge)
-   [Rebase Iterativo](#rebase-iterativo)
-   [Stash](#stash)
-   [Blame](#blame)

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
>
>     git init
>
>   Serve para criar um repositório LOCAL em algum diretório.
>
---
>
>     git remote add origin <URL REMOTE REPOSITORY>
>
>   Serve para conectar um repositório local com o repositório remoto
>
---
>
>     git remote get-url origin
>
>   Devolve a URL do repositório remoto no terminal
>
---
>
>     git remote set-url origin <URL>
>
>  Serve para alterar a origem remota usando URL HTTPS, como por exemplo:
>
>     git remote set-url origin https://devliborio:<app-password>@bitbucket.org/devliborio/git-test-repo.git
>
>     git remote set-url origin <https://<username>:<app-password>@bitbucket.org/<username>/git-test-repo.git> -> (ESTRUTURA)
>
---
>
>     git config --global user.name “username“
>
>  Para adicionar a configuração a todos os repositórios do seu usuário corrente do sistema operacional execute:
>
---
>
>     git config --global user.email “e-mail“
>
>  Para adicionar a configuração a todos os repositórios do seu usuário corrente do sistema operacional execute:
>
---
>
>     git config --local user.name “username“
>
>  Para adicionar a configuração a um repositório local específico, acesse o repositório e execute:
>
---
>
>     git config --local user.email “email“
>
>  Para adicionar a configuração a um repositório local específico, acesse o repositório e execute:
>
---
>
>     git config --system user.name "username"
>
>  Para adicionar a configuração a todos os repositórios de todos os usuários do sistema operacional execute:
>
---
>
>     git config --systema user.email "email"
>
>  Para adicionar a configuração a todos os repositórios de todos os usuários do sistema operacional execute:
>
---
>
>     git <verb> --help ou git <verb> -help
>
>  Serve para te retornar uma documentação do comando que você está com duvida, você coloca o nome do comando no lugar do `<verb>` e escolhe entre a versão 1 com o `--help` para te redirecionar para um site na web com a documentação ou a opção 2 -help que irá te retornar essa mesma documentação só que dessa vez no próprio  terminal.
---
>
>     git add . 
>
>     git add <nomedoarquivo>
>
> Ambos servem para adicionar o arquivo no status de preparo (staged), esse comando é obrigatório para que você consiga realizar o commit.
>
> Apesar dos dois comandos acima terem o mesmo objetivo em comum, os dois também tem diferenças, sendo o 1 acompanhado pelo “ . “ que serve para adicionar TODOS os arquivos de uma vez só para o status (staged), já o 2 exemplo serve para adicionar no status staged somente o arquivo que foi inserido no campo.
---
>
>     git commit -m "<sua mensagem>"
>
> Após o arquivo ser movido para o status de staged ele está pronto para ser commitado, contudo é só usar este comando acompanhado pela mensagem referente a alteração que foi feita.
>
---
>
>     git push -u origin master
>
>     git push
>
> Após ter aplicado o commit você deve querer enviar para a sua plataforma de hospedagem seja o Bitbucket ou o GitHub por exemplo, para isso basta criar uma branch de rastreamento usando o primeiro comando (OBS: só precisa usar essa primeira opção caso seja sua primeira vez fazendo o processo e ainda não tenha uma branch de rastreamento.), caso você já tenha feito isso, basta usar o git push que ele irá enviar seu commit para a plataforma de hospedagem sem problema.
>
---
>
>     git show
>
>  Para visualizar as alterações envolvidas em um determinado commit
---
>
>     git status
>
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

#### **Git hash order:**
>
> `hash commit → hash tree → hash blobs → conteudo do arquivo.`
>
---
>
>     git cat-file -t <pedaço do hash>
>
> Serve para mostrar o tipo da chave hash que estamos querendo saber.
>
---
>
>     git cat-file -p <pedaço do hash>
>
> Serve para mostrar o conteúdo da chave hash pode ser uma tree, blobs.
>
---
>
>     git checkout -b <branch>
>
> Esse comando cria uma nova branch e altera a referência HEAD para a mesma, tornando-a branch corrente.
>
> Porém há outras formas de criar uma branch, sem necessariamente alternar para a recém criada. Para criar uma nova branch a partir da branch corrente, você pode utilizar o comando:
>
>     git branch <nome da nova branch>
>
> Para criar uma nova branch a partir de uma branch especifica utilize o comando
>
>     git branch -c <nome da branch específica> <nome da nova branch>
>
---

>     git branch -a
>
> Ele irá listar todas as nossas branch, tanto as locais que vão estar em branco quanto as de rastreamento que iram estar em vermelho.
>
> E sendo a branch verde com asterisco a nossa branch corrente (branch atual)
>
---
>
>     git branch -m "change username"
>
> Serve para alterar o nome da branch

---

### **Aliases** 

> São usados para criar comandos menores que correspondem a comandos maiores, como segue no exemplo abaixo:
>
>     git config --global alias.hist 'log --pretty=format:"%h %ad | %s%d [%an]" --graph --date=short
>
> Nesse exemplo nosso criamos um alias para acessar o Git log, especificando um pouco o que vamos ter de saída do comando, vamos entender o que é cada estrutura deste comando:
>
> `%h`  = Hash do commit abreviado
>
> `%ad` = Data do commit
>
> `%s` = comentário
>
> `%d` = Decorações do commit (Ex: head de branches, logs)
>
> `%an` = Autor do commit

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
>
>     git config --local push.followTags true
>
> Para adicionar a configuração a todos os repositórios do seu usuário corrente do sistema operacional execute:
>
>     git config --global push.followTags true
>
> Para adicionar a configuração a todos os repositórios de todos os usuários do sistema operacional execute:
>
>     git config --system push.followTags true

---    

### **Descartando Alterações** 

<br>

  #### **Descartando mudanças Locais**

> Fazendo com arquivo já criado
>
>     echo "conteudo do arquivo" > arquivo.txt
>
>     git status
>
>     git restore arquivo.txt -> Ele restaura as alterações
>
>     git status
>
> Fazendo com arquivo novo
>
>     touch arquivonovo.txt
>
>     git status
>
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
>
>     echo "conteudo do arquivo" > arquivo.txt
>
>     touch arquivonovo.txt
>
>     git status
>
>     git add .
>
>     git restore --staged →  Para remover o status de staged e retornar ao status corrente
>
>     git status  → Note que ambos os arquivos que foram enviados para o status staged voltaram ao padrão.
>    
---

 ### **Observação:** 
 
> Além de desfazer alterações, o comando restore também pode ser utilizado para restaurar versões anteriores em um arquivo.
>
> Para isso, você pode utilizar o seguinte comando:
>
>     git restore --source <hash do commit> <nome do arquivo> 
>
---

### **Revert Commit**

> Vamos criar um arquivo novo:
>
>     touch arquivonovo.txt
>
> Agora vamos inserir um conteudo dentro deste arquivo:
>
>     echo "conteudo do arquivo novo" > arquivonovo.txt
>
> Vamos adicionar ele no status de "Staged" usando o comando abaixo:
>
>     git add .
>
> Agora é só fazer o commit:
>
>     git commit -m "novo arquivo arquivonovo.txt"
>
> Agora vamos desfazer esse ultimo commit usando esse comando:
>
>     git revert HEAD --no-edit
>
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
>
>     touch soft.txt
>
>     git add soft.txt
>
>     git commit -m 'adding soft test'
>
>     git hist
>
>     git reset --soft head~
>    
>     git hist
>
>     git status
>
> O parametro soft ele remove o commit e preserva tanto a área de trabalho como também a área de staging, se caso for da nossa preferencia limpar também a área de trabalho e a área de staging usando o parâmetro soft, vamos ter que usar o git restore desse jeito: `git restore --staged soft.txt` e depois `git clean soft.txt -f`

<br>

> Agora vamos entender o **Reset Commit - MIXED**
>
> Vamos adicionar um arquivo chamado `mixed.txt`
>
>     touch mixed.txt
>    
>     git add mixed.txt
>    
>     git commit -m 'adding mixed test'
>    
>     git hist
>    
>     git reset head~
>    
>     git hist
>    
>     git status
>    
> O parâmetro mixed ele remove o commit e preserva somente a área de trabalho, que ao contrario do soft que preserva a área de staging, o mixed remove ele deixando ele no status de untracked. Perceba também que não foi passado nenhum parâmetro no comando `git reset head~` porque por padrão se deixarmos vazio ele obrigatoriamente reconhece o reset como mixed.

<br>

> Agora vamos entender o **Reset Commit - HARD**
>
> Vamos adicionar um arquivo chamado `hard.txt` e nele adicionar o conteudo "hard"
>
>     echo "hard" > hard.txt
>   
>     git add hard.txt
>   
>     git commit -m "adding hard test"
>   
>     git hist
>    
>     git reset --hard head~
>    
>     git hist
>        
> O parâmetro hard ele diferente dos anteriores não preserva nem a área de staging e nem a área de trabalho, descartando totalmente todas as alterações realizadas, o uso convencional dele é geralmente feito para limpar todas as alterações feitas em ambas as áreas com base no ultimo commit.

---

### **Reflog**

> Cenario: Você fez uma `git reset --hard head~` para algumas alterações indesejadas, mas depois percebeu que realmente precisava delas.
> 
> Solução: `git reflog` vem em sua ajuda! É um comando indispensavel para recuperar o histórico de projetos e recuperar quase tudo.
> 
> Agora que sabemos a solução para o nosso problema vamos recuperar o arquivo `hard.txt` com o conteudo "hard".
>
>     git reflog
>   
> Agora pegamos o hash do commit associado ao momento que adicionamos o hard test
>
>     git checkout <commit_hash>
>    
>     dir 
>    
> Pronto agora após usar o comando dir vemos que o nosso arquivo `hard.txt` já foi recuperado, e se usarmos o `cat hard.txt` veremos que o conteudo dele também foi.
>
> Percebam uma peculiaridade, apos executarmos o `git hist` vemos que o HEAD está apontando pro commit e não para master, e a master está apontando pra um commit anterior, algo que prioritariamente está irregular.
>
> Se usarmos o `git status` veremos algo chamado de **Detached HEAD** que ocorreu logo após utilizarmos o checkout em um commit especifico (Nesta situação baseado no reflog)
>
> Vamos revisar o funcionamento da HEAD novamente:
> - O HEAD deve apontar para a branch atual
> - É atraves do HEAD que sabemos em qual branch estamos trabalhando
> - O comportamento normal é o HEAD sempre estar apontando para alguma branch e a branch apontada para o último commit
>
> Depois de revisado esses conceitos basicos podemos entender que ao fazer o checkout diretamente em um commit, o HEAD irá apontar diretamente para um commit
>
> Essa situação caracteriza o processo dito acima denominado de **Detached HEAD**  
>
> A solução para incluir novamente o `hard.txt` dentro da master seria criar uma branch que aponte para o último desses commits e depois fazer um merge com a master. A sequencia de comandos é:
>
>     git branch branch-temp
>    
> No comando acima a branch foi criada apartir do commit em que o `hard test` foi adicionado, ou seja essa branch está apontando para o commit que a gente precisa.
>
>     git checkout master
>    
>     git merge branch-temp -> O git merge traz as alterações de uma branch para outra.
>
>     git merge -d branch-temp
>    
>     git hist
>    
---

### **Merge**

> O merge trata-se de um procedimento de mesclagem que o GIT realiza uma combinação de mudanças de uma branch para outra branch.
> 
> Vamos ver agora um dos tipos de estrategias de merge chamado de **Fast-forward** (Avanço rápido) 
> 
> Iremos criar uma nova branch e fazer checkout nela pra entender melhor como podemos mescla-la com nossa branch principal
>
>     git checkout -b icone
>
>     touch icone.txt
>
>     git add icone.txt
>
>     git commit -m 'adding icon'
>
> Execute o `git hist` na branch icone
>
> Executo o `git hist` na branch master
>
> Perceba que ao realizar o `git hist` em ambas as branchs você entende que após efetuarmos a mudança de branch da master para a icone, a master não evoluiu e todas as alterações só estão sendo efetuadas na branch icone, agora como queremos enviar todas as mudanças feitas na icone para a branch principal e dessa forma faremos:
>
>    git merge icone
>
> Usando o `git merge icone` estamos enviando as alterações da branch icone para a branch master utilizando a estretagia **Fast-forward** (Avanço rápido)

---

 #### **Observação sobre o** `git log`

> Vale destacar que é possível visualizar o log de qualquer branch, mesmo que não seja a branch corrente. Para isso, basta executar:
>
>      git log <nome da branch>
>
>Lembrando que o comando git hist é um atalho criado a partir do git log personalizado. Por isso, o git hist também irá aceitar o nome da branch.
>
>      git hist <nome da branch>

--- 

#### **Merge Three-Way**
>
> Pode também ser chamado de recursiva
>
> Para entender melhor ela vamos fazer o seguinte processo:
> 
>     git checkout -b menu
> 
>     touch menu.txt
> 
>     git add menu.txt
> 
>     git commit -m 'adding menu.txt'
> 
>     git checkout master
> 
> Agora antes de realizar um merge da branch menu para a master vamos gerar um novo commit na branch master também
> 
>     echo 'icone' > icone.txt
> 
>     git add icone.txt
>    
>     git commit -m 'changes in icone.txt'
>
> Agora ao usar o `git hist` tanto na branch master quanto na branch menu percebemos exatamento o ponto onde elas divergem que é logo no ultimo commit feito.
> 
> Vamos fazer um merge para observar o que irá acontecer 
> 
>     git merge menu
> 
> Observe que o git irá abrir o editor de texto padrão para que você insira a mensagem de commit, essa mensagem pode ser chamada de `merge commit`, portanto para esse teste mantenha a mensagem padrão e saia do editor de texto.
> 
> O GIT nesse caso uso da estrategia recursiva (three-way) pois não teria como somente mudar o ponteiro da HEAD. Neste caso seria necessario mesclar o commit feito direto na master, porque lembre-se que foi feito um commit na branch menu e outro na branch master, então para não causar conflitos o merge pega o commit feito na branch menu e mescla com o commit feito na master, esse processo é chamado de estrategia recursiva.
> 
>     git hist
> 
> Após usar o `git hist` percebemos que nosso historico não está tão linear assim e sim meio bifurcado por conta do merge commit, entretando o processo foi efetuado com sucesso e sem conflitos, já sendo possivel que seja empurrada essas alterações para o seu repositorio remoto.

 ---
 #### **Merge No-fast-forward**
 
> Vimos que na primeira estrategia que utilizamos o GIT assumiu que deveriamos usar a técnica fast-forward
>
> No entando, ocassionalmente, você deseja impedir que esse tipo de comportamento ocorra, por exemplo:
>
> Você está mesclando uma ramificação e deseja garantir que quando a branch for incorporada na master, isso esteja visível no seu histórico
>
> Para isso, basta utilizar a opção `--no-ff` no merge
>
> Neste caso o GIT utilizará a técnica recursiva.

---

### **Dag**

> Para falar em Dag precisamos entender que a relação entre commits em um repositorio é baseado em grafos
>
> Grafos é uma área da matemática extremamente importante para a computação, em uma definição simples um grafo é uma estrutura usada para representar um modelo em que existem relações entre os objectos de uma certa colecção.
> <p>
> <img width="250px" src="https://static-02.hindawi.com/articles/jam/volume-2014/948521/figures/948521.fig.0012.jpg" alt="DAG" />
> </p>
>
> A estrutura de uma grafo é relativamente simples onde esses circulos são os Node (Nós) e as linhas as Edge (Arestas) que ligam os Node, como é demonstrado na imagem acima.
>
> Um **grafo direcionado** é uma tipo de grafo em que os nós estão conectados em uma determinada direção
>
> #### **Grafos Aciclicos**
>
> São grafos onde não há ciclos ou não circulares, como mostrado no exemplo abaixo:
> <p>
> <img width="250px" src="https://i.stack.imgur.com/xeOJv.png" alt="DAG" />
> </p>
>
> <br>
>
> #### **Grafos Ciclicos**
>
> São grafos onde há a existencia de cliclos circulares, como demonstrado abaixo:
> <p>
> <img width="250px" src="https://static-02.hindawi.com/articles/jam/volume-2014/948521/figures/948521.fig.0013.jpg" alt="DAG" />
> </p>
>
> <br>
>
> #### **Grafo acíclico dirigido** (DAG)
>
> É um tipo de grafo que atende as seguintes características: **direcionado** e **acíclico**
> <p>
> <img width="250px" src="https://w7.pngwing.com/pngs/756/246/png-transparent-data-structure-binary-tree-computer-science-binary-search-tree-acyclic-directed-graph-angle-white-symmetry.png" alt="DAG" />
> </p>
>
> <br>
>
> #### **DAG x GIT**
>
> O GIT modela a relação dee commits com o grafo acíclico dirigido (DAG)
>
> Cada node (nó) representa um commit
>
> As setas apontam **para os pais** de um commit
>
> Na ilustração acima podemos notar que por exemplo o node / commit (1) pode ser definido como um commit de merge, porque ele tem dois pais sendo eles o 2 e o 3.

---

### **Conflitos**

> Os conflitos surgem em situações de mesclagem em que o GIT não pode determinar automaticamente o que está correto e é necessario decisões humanas
>
> É importante destacar que não é necessario dois desenvolvedores no projeto para que existam conflitos, duas branchs criadas pelo mesmo desenvolvedor também podem gerar conflitos.
>
> Os conflitos afetam apenas o desenvolvedor que conduz a mesclagem, o resto da equipe não tem conhecimento do conflito.
>
> O GIT marcarará o arquivo como conflitante e interomperá o processo da fusão (merge). É responsabilidade dos desenvolvedores resolver esse conflito.
>
> Para entendermos melhor vamos gerar um conflito:
>
>     echo -e 'consulta web service\nloga' > login.txt -> Esse -e serve para que possa ser interpretado esse /n para quebrar a linha.
>
>     git add login.txt
>
>     git commit -m 'login algorithm'
>
>     git checkout -b login-persist
>
> Altere o arquivo `login.txt` adicionando na terceira linha o conteúdo "salva na tabela" 
>
>     echo "salva na tabela" >> login.txt -> >> insere no final do arquivo
>
>     git add login.txt
>
>     git commit -m "including persist on login.txt"
>
>     git checkout master
>
> Altere o arquivo login.txt adicionando na terceira linha o conteúdo "gambiarra"
>
>     echo "gambiarra" >> login.txt
>
>     git add login.txt
>
>     git commit -m "emergency adjustment"
>
>     git merge login-persist
>
> Perceba que ao tentar efetuar o merge da branch login-persist o git retorna um conflito que tem que ser resolvido.
>
>     git status
>
> Após usar o `git status` você percebe que tem alterações que devem ser feitas no arquivo `login.txt` e para isso abra o arquivo no editor de código da sua preferencia, no meu caso abri o Visual Studio Code e ao abrir você ira perceber que ele mostrar as linahs que desenvolveram esse conflito e você tem algumas opções entre manter o commit de entrada, manter os dois commits ou manter o ultimo commit que foi feito, no meu caso escolhi manter os dois commits, após isso salve as alterações e o seu conflito já deve ter sido resolvido.
>
> Agora adicione novamente o arquivo `login.txt` a área de staging e depois efetue o commit
>
>     git add login.txt
>
>     git commit -m "resolving login conflict"
>
>
> Depois desses passos feitos as alterações no arquivo e no conteudo dele já podem ser subidas para o repositorio remoto usando o `git push`
>
>     git push

---

### **Trabalho Colaborativo**
<br>

#### **Simulando um segundo colaborador**

> Agora vamos simular outro contribuidor atuando no projeto, fazendo um novo clone do repositorio.
>
>     git branch -a
>
> É interessante notar que no novo repositorio a única branch local que existe é a da master.
>
> Agora vamos criar nosso primeiro commit nesse novo repositorio.
>
>     touch logo.txt
>
>     git add logo.txt
>
>     git commit -m "adding logo.txt"
>
>     git push

<br>

#### **Fetch**

> Agora no repositorio principal vamos executar um comando:
>
>     git fetch
>
> O fetch fará download do conteúdo remoto, mas não atualizará o estado de funcionamento do seu repositorio local, deixando intacto o trabalho atual.
>
> Ou seja, nesta situação nossa área de trabalho se manteve intacta, novo GIT Objects foram baixados e a branch de rastreamento da master está apontando para o último commit feito no tópico anterior `login.txt`
>
> Para visualizar as alterações execute:
>
>     git checkout origin/master
>
> Executamos esse comando somente para visualizar as alterações na master remota
>
> Para trazer as alterações para a master local faça o procedimento seguinte:
>
>     git checkout master 
>
>     git merge --no-ff origin/master
>
>     git hist
>
> Apos executar o `git hist` vemos que foi efetuado o commit de merge e usando o `ls` ou `dir` veremos também que o arquivo `logo.txt` também ira constar na branch principal. 

---
#### **Pull**

> O GIT pull baixa as alterações do repositório remoto e mescla com a sua área de trabalho
>
> Vamos alterar o conteudo do arquivo `logo.txt`
>
>     echo "logo" > logo.txt
>
>     git add logo.txt
>
>     git commit -m "changes in logo.txt"
>
>     git push
>
> Agora no repositório do outro colaborador vamos usar o `git pull` para receber as alterações que fizemos no conteudo do `logo.txt`.
>
>     git pull
>
>     git hist
>
> Com a execução do `git hist` podemos observar que o commit que acabamos de fazer no repositório principal já está incluso no repósitorio do outro colabroador ou seja o GIT baixou e fez o merge da branch de rastreamento `origin/master` pra branch local `Master`, e observe também que não teve nenhum commit de merge porque foi feito com a estratégia `Fast-forward`

---

#### **Bloqueio de Push**

> Para demonstrar essa situação vamos executar a seguinte situação:
>
> No repositorio local do outro contribuidor vamos criar um arquivo, commitar e enviar para o repositório remoto.
> 
>      touch dadospessoais.txt
>
>      git add dadospessoais.txt
>
>      git commmit -m 'adding dadospessoais.txt'
>
>      git push
>
> Agora vamos voltar ao nosso repositório principal e criar outro commit e tentar enviar para o repositorio remoto
>
>       touch dadospublicos.txt
>
>       git add dadospublicos.txt
>
>       git commit -m 'adding dadospublicos.txt'
>
>       git push
>
> Notem que o push foi bloqueado porque existe um commit do "outro contribuidor" que ainda não foi baixado no seu repositorio local. Nesta situação o GIT pede que você faça um pull antes, pois caso exista conflito de merge este será o momento de resolver
>
>       git pull
>
> Não houveram conflitos pois o merge foi realizado com arquivos diferentes, tendo isso em mente vamos empurrar para o repositório remoto
>
>       git push

---

### **Rescrevendo o histórico**
<br>

#### **Rebase**

> Agora vamos entender como funciona o rebase, ele tem a mesma finalidade de um merge por exemplo, mas contudo de uma forma muito diferentes do merge.
>
> Vamos ver melhor o que foi dito na pratica:
>
> Entre no repositorio principal e crie uma branch, crie um arquivo e commite ele
>
>       git checkout -b notificacoes
>
>       touch notificacoes.txt
>
>       git add notificacoes.txt
>
>       git commit -m "adding notificacoes.txt"
>
>       git hist
>
> Após executar o `git hist` vemos que a HEAD está apontando para nossa branch notificacoes que está apontando pro nosso commit que acabamos de fazer
>
> Agora vamos retornar a branch master e modificar o conteudo do arquivo `menu.txt` e depois commitar ele.
>
>        git checkout master
>
>        echo "menu" > menu.txt
>
>        git add menu.txt
>
>        git commit -m "changes in menu"
>
>        git hist
>
> Agora ao executar o `git hist` vemos que o HEAD aponta pra master que aponta pro commit onde mudamos o conteudo do `menu.txt`
>
> Agora vamos retornar a branch notificacoes e fazer um rebase na branch notificacoes
>
>         git checkout notificacoes
>
>         git rebase master
>
>         git hist
>
> Vamos entender como funciona o comando rebase, basicamente ele irá pegar o commit que foi feito na branch notificacoes e vai recriar ele na ponta da branch master, se você parar pra pensar é como se ela fosse criada a partir da branch master no ultimo commit feito, que foi no conteudo do `menu.txt`
>
> Ou seja agora que executamos o `git rebase` a branch notificacoes tem como o ultimo commit o 'adding notificacoes' e graças ao rebase anteriormente a esse commit temos o commit de mudanças no conteudo no arquivo `menu.txt`.
>
> Note também que ao executar o `git hist` a hash do commit "adding notificacoes" foi alterada.
>
> Um observação importante é que o commit foi recriado e inserido na ponta mantendo um histórico linear, perceba que essa era uma situação classica de estrtagia recursiva caso fosse efetuado um merge, que iria gerar um merge commit gerando um historico bifurcado em vez de linear, o problema de um historico cheio de merge recursivo é que pode ficar muito dificil de entender, diferente de um historico linear.
>
> Agora após fazer o rebase na branch notificacoes vamos voltar a master e fazer um merge Fast-forward
>
>          git checkout master
>
>          git merge notificacoes
>
>          git hist
>
> Pronto, finalizamos o processo, deixando ambas as branchs igualmente equiparadas.

--- 

 #### **The golden rule of rebase**

> Depois de entender os conceitos envolvidos no Rebase é extremamente importante saber qundo não utilizar este comando
>
> A regra de ouru do Rebase é:
>
> **Não recrie commits que existam fora do seu repositório e nos quais as pessoas possam ter trabalhado** 

---

 #### **Merge x Rebase**

> O merge é uma **operação não destrutiva**. As ramificações existentes não são alteradas de forma alguma. Isso evita todas as possiveis armadilhas do rebase.
>
> Por outro lado, em caso estrategias recursivas significa a existência de bifurcações, o que irá poluir o histórico do projeto.
>
> O rebase é uma **operação destrutiva**. Um ou mais commits serão eliminados e criados novamente.
>
> Por isso, para não gerar problemas maiores que um histórico poluído, é importante seguir a regra de ouro do rebase. Se você utilizar esse comando de forma consciente você terá um histórico mais linear e fácil de ser entendido.
>
> Ou seja se você preferir um histórico limpo e linear, sem confimações desnecessárias de mesclagem utilize `git rebase` ao invés de `git merge`.
>
> Por outro lado, se você deseja preservar o histórico completo do seu projeto e evitar o risco de reescrever commits publicos, você pode utilizar o `git merge`.

---

#### **Emendar Commit**
> 
> Pense que você fez um commit e depois percebeu que esqueceu de commitar alguma coisa, algum arquivo por exemplo, faria todo sentido que essa alteração que você esqueceu, estar no commit anterior em vez de um novo commit.
>
> Para entendermos melhor essa situação vamos fazer isso na pratica
>
> Vamos criar uma branch e fazer um commit nela:
>
>          git checkout -b brindes  
>
>          touch brindes.txt
>
>          git commit -m 'adding brindes.txt'
>
>          git hist
>
> Agora vamos adicionar um conteudo no arquivo brindes.txt
>
>           echo "meus brindes" > brindes.txt
>
>           git add brindes.txt
>
>           git commit --amend -m "adding brindes.txt with content"
>
>           git hist
>
> Percebem que quando fui fazer o commit, eu usei o parametro `--amend` que basicamente adicionou o conteudo "meus brindes" ao commit anterior que fizemos no primeiro exemplo, e note que esse primeiro commit não existe mais, porque com o uso do `--amend` ele foi recriado com as alterações do conteudo do arquivo `brindes.txt`.

---

#### **Squash Merge**
>
> O parâmetro `git merge --squash` ele junta dois commits por exemplo em um unico commit, vamos ver isso melhor na pratica.
>
> Vamos ir para o nosso repositório principal e ir para a branch master, apartir disso vamos criar uma nova branch, criar um novo arquivo e commitar:
>
>             git checkout master
>
>             git checkout -b esquecisenha
>
>             touch esquecisenha.txt
>
>             git add esquecisenha.txt
>
>             git commit -m "adding esquecisenha.txt"
>
> Agora vamos inserir um conteudo no arquivo esquecisenha.txt e commitar:
> 
>              echo 'esqueci a senha codigo' > esquecisenha.txt
>
>              git add esquecisenha.txt
>
>              git commit -m "finishing forgot my password"
>
>              git hist
>
> Após feito isso, vamos retornar a branch master e executar o `git merge --squash` na branch esquecisenha
>
>              git checkout master
>
>              git merge --squash esquecisenha
>
>              git commit -m "adding forgot my password feature"
>              
>              git hist
>
> Perceba que ao executar o `--squash` ele retorna um aviso que diz `"squash commit -- not updating HEAD"`, isso porque o GIT está esperando que a gente faça o commit da união dos dois commits do branch esquecisenha. Pra ficar mais claro, ele basicamente pegou as alterações desses dois commits da branch esquecisenha e colocou na área de preparo (staged), tanto que se você efetuar um `git status` você verá um arquivo na área de preparo que já contem tantos as alterações no conteudo, quanto a da criação do proprio arquivo.

---

#### **Rebase Iterativo**
>
> O rebase iterativo faz com que ao invez de mover cegamente todos os commits para a nova base, oferece a oportunidade de alterar os commits individualmente no processo
>
> Para usar esse o `git rebase` utilize o parâmetro `--i`
>
> Perceba que ao executar o comando será aberto um editor padrão definido pelo GIT no qual você poderá inserir comandos para cada commit a ser rebaseado. Esses comandos determinam como os commits individuais serão transferidos para a nova base.
>
> Para entender melhor, vamos praticar, vamos criar uma branch nova e efetuar varios commits
>
>     git checkout -b promocoes
>
>     touch promocoes.txt
>
>     git add promocoes.txt
>
>     git commit -m "adding promocoes.txt"
>
> Agora vamos adicionar um conteudo no arquivo `promocoes.txt`
>
>     echo "codigo finalizado de promoções" > promocoes.txt
>
>     git add promocoes.txt
>
>     git commit -m "finishing promotions development"
>
> Agora vamos alterar o conteúdo do arquivo `promocoes.txt` 
>
>     echo "código finalizado de promoções sem bugs" > promocoes.txt
>
>     git add promocoes.txt
>
>     git commit -m "bugs xixes"
>
> Agora vamos sobrescrever o conteúdo do arquivo `promocoes.txt`.
>
>     echo "inclusão de gambiarra" > promocoes.txt
>
>     git add promocoes.txt
>
>     git commit -m "adding bad workaround"
>
> Vamos executar o `git hist` agora.
>
>     git hist
>
> Para executarmos o rebase iterativo nos 4 ultimos commits que fizemos teremos que escolher a referencia do ultimo commit anterior a eles, se no caso você não estiver na sua branch principal e quiser alterar o ultimo commit que foi feito nela, execute somente um `git rebase -i master` vamos fazer isso.
>
>     git rebase -i master
>
> Após aberto o seu editor padrão vamos entender alguns conceitos sobre os comandos que vamos executar nos commits:
>
> `p, pick <commit>` = usar commit.
>  
> `r, reword <commit>` = usar commit, mas edite a mensagem do commit.
>
> `d, drop <commit>` = remover commit.
>
> `s, squash <commit>`= usar commit, mas mesclar em commit anterior. 
>
> Entendido os conceitos de alguns dos vários comandos do rebase iterativo, vamos aplica-los nos 4 commits que fizemos.
>
> No primeiro commit que fizemos: `adding promocoes.txt` vamos usar o comando `pick`.
>
> No segundo commit que fizemos: `finishing promotions development` vamos usar o comando `squash` para fundir ou mesclar ele no primeiro commit.
>
> No terceiro commit onde fizemos: `bugs xixes` vamos usar o comando `reword` para consertar o erro de ortografia "xixes" para "fixes".
>
> No quarto commit onde fizemos: `adding bad workaround` vamos usar o comando `drop` para deletar esse commit.
>
> Após escolher os comandos a serem utilizado em cada commit, iram abrir duas janelas de requisiçao do seu editor padrão do GIT.
> - Uma para inserir a mensagem de commit da fusão do segundo commit com o primeiro.
> - E a outra para editar a mensagem do terceiro commit onde em vez de `bug xixes` ira ser `bug fixes`. 
>
> Agora após efetuadas todas as alterações vamos voltar para branch master e fazer um merge da branch promocoes e realizar um push para o repositorio remoto. 
>
>     git checkout master
>
>     git merge promocoes
>
>     git push
>
> Pronto finalizamos os ensinamentos de rebase iterativo.

---

### **Outros conceitos e comandos**
<br>

#### **Stash**
> 
> O comando git stash salva as alterações sem commit (tanto as preparadas quanto as não preparadas) para uso posterior.
>
> Vamos entender melhor o seu uso na pratica:
>
> Vamos criar uma nova branch e mudar para ela
>
>      git checkout -b noticias
>
> Agora vamos criar um arquivo com um conteudo dentro dele.
>
>     echo "minha primeira noticia" > noticias.txt
> 
> Agora adicionar a área de preparo e commitar
>
>     git add noticias.txt
>
>     git commit -m "adding noticias.txt"
>
> Agora inserir outro conteudo em outra linha dentro do `noticias.txt`
>
>     echo "minha segunda noticia" >> noticias.txt
>
> Agora vamos tentar voltar para a branch master
>
>     git checkout master
>
> Perceba que retornou um erro, porque na branch master o arquivo `noticias.txt` não existe. Como houveram modificações, se o GIT deletar este arquivo suas modificações serão perdidas.
>
> Nesta situação o GIT está pedindo par que você commit suas mudanças ou que faça um `git stash` 
>
> O comando `git stash` salva suas modificações locais em uma pilha e limpa sua área de trabalho para o ultimo commit feito.
>
> Agora que já sabemos o que fazer, vamos executar o `git stash`
>
>     git stash
>
> Se não for passado nada no comando `stash` ele vai por padrão executar um `push`
>
> Agora vamos executar um `git stash list`, que vai mostrar o estado da pilha, e as entradas que foram feitas nela, vamos poder notar que a ultima modificação que foi feita está contida na pilha, que no caso é a inserção da segunda linha chamada `minha segunda noticia`.
>
> Agora que a área de trabalho está limpa, como mostrado no `git status`, podemos voltar para branch master sem maiores problemas.
>
>     git checkout master
>
> Outra observação sobre o `git stash` é que por padrão arquivos com status untracked (que não são monitorados pelo GIT) não são salvos no `stash`, mas você pode usar `--include-untracked` para forçar que arquivos com esse status sejam salvos.
>
> Agora dando continuidade ao nosso exercicio pratico com o `git stash` vamos retornar para a branch de noticias.
>
>     git checkout noticias
>
> E agora vamos puxar novamente as alterações que salvamos com o git stash para nossa área de trabalho usando o seguinte comando
>
>     git stash pop
>
> E também podemos notar com o comando `git stash list` que a pilha está novamente vazia, já que retiramos o unico conteudo que estava salvo lá.

---

#### **Blame**
>
> Com o comando `Blame` podemos verificar qual commit e autor modificaram pela útima vez cada linha de um arquivo.
>
> Para tornar mais simples o entendimento vamos criar um arquivo, inserir um conteudo nele e commitar, logo após vamos usar o `git blame`
>
>     touch culpa.txt
>
>     echo "eu alterei" > culpa.txt
>
>     git add culpa.txt
>
>     git commit -m "adding culpa.txt" 
> 
> Após efetuada essa primeira etapa, vamos usar o `git blame` para vermos o que acontece
>
>     git blame culpa.txt
>
> Veremos que o GIT retorna o responsavel, a data, e o hash do ultimo commit abreviado.

---

### **Bisect**