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

-  De volta no Git Bash, podemos colocar no Stage apenas arquivos novos e modificados.

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

