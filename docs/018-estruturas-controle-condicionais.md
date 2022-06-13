# **Estruturas de controle**
As estruturas de controle são parte de um código que é executado com base em algum teste lógico. Existem vários tipos de estruturas controle utilizadas para tomar uma decisão e nesse tópico vamos tratar apenas das [condicionais](/docs/09-conditionals.md).  

Uma curiosidade sobre as estruturas de controle é que sempre que formos usá-las, usaremos também algum tipo de operador, principalmente quando se trata de mais de um parâmetro onde é bastante os operadores de comparação e operadores lógicos.

## **Condicionais**
Como dito, uma estrutura de controle é baseada em um teste lógico para tomar uma decisão. E já dito também que usamos operadores lógicos para montarmos essas estruturas.  
Até aqui, ok. Mas, quando falamos de condicionais, nós tratamos de colocar uma condição para o nosso teste decidir e vamos ver quais são essas condições aqui.  

### **Condição if/else**  
Já passamos por essa condição algumas vezes, e é a mais conhecida dentre as condições. Vamos ver um exemplo antes de comentar sobre ela.  

```php
<?php

$task = "completed";

if($task == "completed") {
    echo "Sua tarefa está feita!";
} else {
    echo "Sua tarefa está incompleta.";
}
```

No bloco de código acima é possível vermos que temos uma variável com um valor atribuído a ela. Quando vamos colocar esse valor em uma condição, utilizamos algum operador de comparação.  

No caso do nosso código, seguimos a seguinte lógica: SE (if) a nossa tarefa estiver concluída, ou seja, se o valor da nossa task for igual (==) a ```completed```, então, nosso código fará algo. Ele irá retornar que a tarefa está feita. Caso contrário (else), ele irá retornar que a tarefa ainda não foi concluída.  

Um ponto para analisarmos é que uma condicional trabalha com valores verdadeiros ou falsos. E a nossa primeira condição será a condição verdadeira, pois, após a verificação temos um resultado verdadeiro; caso esse resultado não for verdadeiro vamos para a segunda condição, no else.  

* **Utilizando dois parâmetros**  
Quando vamos verificar mais de um parâmetro em uma condição utlizamos os operadores lógicos para nos ajudar. Vejamos um exemplo.

```php
<?php

$user = "BelliniHe4rt";
$password = "pass123";

if($user == "BelliniHe4rt" && $password == "pass123") {
    echo "Seja bem-vinda a sua conta.";
} else {
    echo "Nome de usuário ou senha incorretos.";
}
```

Interpretando o nosso bloco de codigo entendemos o seguinte: temos um caso de login onde são atribuídos para duas variáveis diferentes o valor de um usuário e a senha para que o login seja feito.  

Na nossa condição vemos o seguinte: SE o valor do nosso usuário for o mesmo do que o valor atribuído à variável do usuário **E** o valor da nossa senha for o mesma do valor atribuído à variável da senha, então, temos a nossa primeira condição que é a verdadeira e assim por diante.  

Bem, não há nenhum segredo em utilizar mais de um parâmetro na nossa condição, como vimos acima. Utilizamos o operador **E** para checar se ambas as condições eram verdadeiras.  

### **Condição if/else if/else**  
Quando temos mais de uma opção ou condição verdadeira, utilizamos o **else if** para abrir outras condições. Vamos usar o último exemplo para continuar com a mesma linha de raciocínio.

```php
<?php

$user1 = "BelliniHe4rt";
$password1 = "pass123";

$user2 = "SomeoneHe4rt";
$password2 = "senha123";

if($user1 == "BelliniHe4rt" && $password1 == "pass123") {
    echo "Seja bem-vinda a sua conta.";
} else if($user2 == "SomeoneHe4rt" && $password2 == "senha123") {
    echo "Seja bem-vindo a sua conta.";
} else {
    echo "Nome de usuário ou senha incorretos.";
}
```

No exemplo em que utilizando mais de um parâmetro, colocamos uma condição verdadeira para verificarmos. Entendemos assim a estrutura if/else, uma condição verdadeira e uma falsa. Mas, ainda temos a opção de ter mais de uma condição verdadeira, e foi isso o que fizemos no bloco de código acima.  

Quando abrimos a nossa condição, verificamos o usuário 1. Mas, vejamos te temos agora um usuário 2 para verificar antes de declarar a nossa condição falsa (else). Para verificarmos o usuário 2 nós utilizamos o ***else/if***, o que nos permitiu uma segunda condição verdadeira antes de fecharmos a estrutura.  

### **Condição switch-case**
Essa condição é uma condição de casos de uso, o que é bem parecido com a condição if/else e else-if. O curioso e interessante dessa condição é que sua estrutura lembra muito também o design de menus de jogos antigos.  

Em questões de estrutura, podemos dizer da similaridade com menus de jogos antigos, mas, principalmente podemos dizer isso porque essa é uma condição de casos de uso. Ou seja, é possível fazer menus com esse tipo de condição. Vejamos um exemplo.

```php
<?php

$sabores = "!chocolate";

switch($sabores){
    case "!chocolate":
        echo "Você escolheu o sabor chocolate para o seu sorvetinho!";
        break;
    case "!maracuja":
        echo "Você escolheu o sabor maracujá para o seu sorvetinho!";
        break;
    case "!morango":
        echo "Você escolheu o sabor morango para o seu sorvetinho!";
        break;
    default:
        echo "Você não escolheu nenhum sabor para o seu sorvetinho :(";
        break;

```

Suponhamos que estamos em um menu online do cardápio de uma sorveteria. Bem, no cóodigo acima foi o que fizemos de exemplo. Nós temos N opções de sabores, mas, se escolhermos uma delas, nos será retornado que escolhemos tal sabor.  

Quando falo que se pode fazer menus com a condição switch-case, pode-se fazer vários tipos de menus. Esse foi apenas um dos N exemplos que poderia ser usado.