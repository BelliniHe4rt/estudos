# **1. Git e GitHub**
  Aqui iremos tratar um pouco sobre ```git``` e o GitHub.  
  Aprender como a usar essas duas coisinhas pode mudar totalmente o rumo dos seus estudos e das suas documentações. Por exemplo, decidi colocar todas as minhas anotações de estudos em um repositório no GitHub.  

  ***Mas, Bellini, por que você não começou a fazer isso logo que começou os seus estudos?***  
  Bem, digamos que só pensei nisso depois de começar os estudos e achei interesante documentá-los de alguma forma para que eu mesma pudesse consultar se precisasse e com o intuito de poder ajudar outras pessoas através dessas anotações também, desta forma deixando tudo o que estudo em open source.  
  
  Mas, vamos ao ponto deste documento. **O que é o git?**  
  O git é uma extensão entre o nosso computador e o GitHub para formarmos repositórios, entre outras coisas, e para implementar isso de forma open source ou não na nossa plataforma e no nosso perfil.  
  A forma da qual usamos o que pode ser indireta ou direta (mas, visando bem, poderíamos dizer que ambas são usadas de forma direta; o que muda é a interface, sendo gráfica e muito mais fácil de usar ou podemos utilizar um editor de texto direto no nosso computador).    

  Quando vamos utilizar o git pela **plataforma do GitHub¹**, a interface gráfica facilita o uso do git, pois não precisamos digitar código algum e temos os "botões" nos idicando o que fazer e onde fazer, tudo com apenas um clique.  
  Quando estamos no nosso computador, utilizamos o terminal para executar os comandos do git.   

  <small>¹A plataforma do GitHub é onde conseguimos utilizar a interface gráfica, seja pelo site ou o aplicativo para o computador. </small>  
  
  ## Comandos de git    
  Aqui eu vou mostrar um pouco desses comandos e o que eles fazem (e também deixar alguns "erros de gravação" de quando utilizei git pelo terminal). Para ser mais direta, mostrarei os três principais comandos que usamos no git e outros dois de brinde. 

  * ### git clone
  O comando *git clone* nos permite clonar um repositório inteiro para alguma pasta dentro do nosso computador. Nessa pasta ficará o repositório que clonamos, em formato de outra pasta. Para utilizarmos esse comando precisamos copiar o link do nosso repositório e colocar logo depois de digitar o comando, ficando assim, por exemplo:  

  ```
  Bellini@DESKTOP-USK0Q7G:~ git clone git@github.com:BelliniHe4rt/estudos.git
  ```

  Quando vamos clonar nosso repositório é importante lembrar dentro de qual pasta estamos no para clonar o nosso repositório, pois é dentro dela que ele ficará.
  
  * ### git init
  Com o com comando *git init* nós "iniciamos" o nosso repositório na nossa no computador para poder seguir e utilizar-mos ele. Sua sintaxe é a seguinte:

```
Bellini@DESKTOP-USK0Q7G:~ git init 
```

É importante lembrar de sempre iniciar o repositório depois que ele é clonado, para poder utilizar os próximos comandos. A minha primeira "falha na matrix" e "erro de gravação" foi justamente por esquecer de dar um *git init* no meu repositório e ficar sempre dando erro quando ia dar um *push* (veremos a seguir).

* ### git add
Quando alteramos alguma coisa no nosso repositório, precisamos adicionar essas alterações no repositório depois de salvar. Para isso serve o comando *git add*, assim ficando com a seguinte sintaxe:

```
Bellini@DESKTOP-USK0Q7G:~ git add .
```

Quando utilizamos o **.** após o comando, significa que estamos pegando **toda** a informação do nosso arquivo ou do nosso repositório, e aqui nesse caso estamos adicionando **toda** a informação do nosso arquivo e adicionando ao nosso repositório.

* ### git commit
Para confirmar que adicionamos as informações alteradas ou adicionadas do arquivo ao nosso repositório, utilizamos o *git commit* e falamos que estamos "commitando" as informações do nosso arquivo. A sintaxe é a seguinte:

```
Bellini@DESKTOP-USK0Q7G:~ git commit -m "Descrição da alteração"
```

Sempre que commitamos uma alteração, precisamos indicar o que fizemos. Em um projeto open source precisamos sempre deixar claro para o nosso leitor o que está acontecendo no nosso código, no nosso repositório, em tudo! Semântica, organização e clareza são duas coisas importantíssimas no mundo open source.

* ### git push
E para finalizar esse processo de alteração ou adição de algo ao nosso repositório precisamos enviar o nosso repositório de volta para a plataforma do GitHub ou salvar ele, então damos um *git push* no nosso terminal e finalizamos tudo, mas, ainda temos uma última curiosidade para saber depois de sabermos a sintaxe.

```
Bellini@DESKTOP-USK0Q7G:~ git push origin main
```

Primeiro, quando estamos usando markdown no nosso editor (no meu caso, uso o VS Code) para alterarmos o nosso arquivo, precisamos utilizar o terminal para adicionar, commitar e dar push no nosso repositório, porque não estamos utilizando a interface gráfica, e nesse processo temos duas coisas interessantes para saber:

1. Quando o nosso computador não está autorizado na plataforma do GitHub para fazer os git add, commit e push, nos é solicitado um usuário e senha para podermos continuar com a nossa ação e finalizar ela (nisso utilizamos só git push);
2. Quando nós autorizamos uma chave na plataforma do GitHub para que o nosso computador possa ter acesso direto ao GitHub, nós fazemos como no exemplo acima, o que significa que estamos mandando um arquivo diretamente do nosso computador (origin) para a branch main do GitHub.

## **Conclusão**
Para entrarmos no mundo open source e podermos compartilhar nossos projetos com outras pessoas dando acesso para que elas possam nos sugestionar alterações e melhorias utilizamos muito o git e GitHub. Um dos aprendizados mais interessantes e importantes até agora nessa jornada foi sobre semântica e organização, o que facilita muito a leitura do nosso código para quem vai editar, etc. E outra coisa importantíssima que aprendi a usar também foi o tal do markdown, pois é através dele que faço todas as minhas anotações e artigos de estudo.  
Se querem uma dica, semântica e markdown são pontos principais para se começar a aprender antes de entrar diretamente no mundo dev, e são coisas que as pessoas não dão tanta atenção, mas, fazem TODA a diferença.