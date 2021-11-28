# Criando o Diretório <h2>

Primeiro passo é a criação das pastas na sua maquina.
Em nosso exemplo, criamos no Documentos as seguintes pastas:

***C:\Users\Usuario\Documents\Dev\Git\Dio***

Nosso diretório do GitHub será clonado para a pasta Dio na maquina.

# Criando diretório no Github <h2>

Conforme na imagem a seguir, crie o diretório.

![Exemplo](https://i.imgur.com/KfiCZCC.png)

Para o próximo passo, precisaremos do link do diretório criado.

Para isso, siga conforme na imagem:

![Passo 1](https://i.imgur.com/qPRETh1.png)

# Iniciando Comandos no Bash

Acesse o programa de terminal Git Bash em sua maquina. Localize a pasta que criamos no começo desse arquivo.

Possível ao abrir o Bash, estará numa pasta padrão. 

- Abra a pasta do *Documents\Dev\Git\Dio* da seguinte forma:

~~~bash
$ cd Documentos\Dev\Git\Dio
~~~

- Clonando o diretório do Github para a pasta na Dio na maquina. A URL é a mesma informada no ***Passo 1***

~~~bash
$ git clone https://github.com/andressansantos/dio-desafio-github-primeiro-repositorio.git

~~~

- Para saber se há alguma atualização, podemos rodar o status.

~~~bash
$ git status
~~~

- Acesse a pasta ***\Dio*** e abra o README.md. Por ele, poderá colocar a introdução do seu projeto utilizando o Markdown. Salve o mesmo.

-  De volta no Git Bash, podemos colocar no Stage todos arquivos (novos, modificados e removidos) no index/stage

~~~bash
$ git add .
~~~

- Realize o primeiro commmit. O que fica entre aspas, deve ser a observação que deseja, caso em algum momento precise voltar atás nas alterações feitas.

~~~bash
$ git commit -m "Atualização README"
~~~

- Por fim, envie para o Github com o comando push. Fazendo isso, será atualizado todos os arquivos no site, caso algum tenha sofrido alteração em sua maquina.

~~~bash
$ git push origin main
~~~

# Observações Comando Git Add <h2>

Os comandos ***git add --all*** e ***git add .***, podem parecer iguais mas fazem ações bem diferentes:

- ***git add --all***: adiciona ao staging arquivos desde a raiz do repositório passando por todos os subdiretórios, e aqui está a diferença, não importa se você está na raiz ou no sub-diretório.

- ***git add .***: usando o ponto, será adicionado ao stagging somente os arquivos a partir do diretório que você está, e os sub-diretórios deste.

Exemplo:

Usando a seguinte estrutura de arquivos e pastas como exemplo:

(https://i.imgur.com/M1eHn30.png)

Considerando que somente o .gitignore está versionado no repositório, se você estiver no diretório src/Views/Home e executar:

~~~bash
$ git add .
~~~

Serão adicionados os arquivos: About.cshtml, Contact.cshtml, Index.cshtml e Privacy.cshtml. Mas não serão adicionados os arquivos de outros diretórios, por exemplo: HomeController.cs, que está no diretório src/Controllers/.

- ***git add * (asterisco)***: vai funcionar exatamente igual ao comando anterior, adicionando somente os arquivos da pasta corrente ao que o comando foi executado.

- ***git add -u***, ou ***git add --update*** vai fazer um update na stagging nos arquivos que já estão sendo rastreados pelo Git.

Continuando a usar o exemplo anterior, depois de executar o ***git add .*** e em seguida ***git commit -m "Primeiro"***, ainda existirão arquivos a serem adicionados ao respositório; então, edita-se o arquivo ***About.cshtml***. Executando um ***git status***, o estado do repositório será:

(https://i.imgur.com/4s739nJ.png)

Executando o comando ***git add -u***, somente o arquivo ***About.cshtml*** é colocado na área de staging, os outros arquivos que ainda não estão no repositório continuam como não rastreados pelo Git. Esse comando vai funcionar tanto para arquivos modificados como para apagados.

[Fonte da Observação](https://pt.stackoverflow.com/questions/326160/diferen%C3%A7a-entre-git-add-all-git-add-e-git-add-u)