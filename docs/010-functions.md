# Funções
No ensino médio aprendemos vários tipos de funções matemáticas. Aqui vamos falar sobre o que é uma função dentro do contexto de programação.  
Na escola sempre vimos algumas fórmulas que nunca mudaram, e nós sempre alteramos o valor e fazemos algum cálculo dentro delas. Bom, aqui em programação podemos usar o conceito dessas fórmulas para explicar o que seria uma função.  

Assim como as fórmulas são reutilizáveis, uma função é um pedaço de código que pode ser usado mais de uma vez. Isto é, a função permite que passemos parâmetros diretamente para algo que está pronto. Não precisamos pensar muito na lógica de algo já feito.  

Vamos ver um exemplo na prática para entender como funciona.  

```php
<?php

$name = (string)fgets(STDIN);
$age = (int)fgets(STDIN);

function ageCheck(int $age): string
{    
    if ($age >= 18) {
        return "Welcome in!" . PHP_EOL;
    } else {
        return "Sorry! You're not allowed." . PHP_EOL;
    }

}

$printCheck = ageCheck($age); 

echo $printCheck;
```

Ok! Acima temos um código completo usando uma função como exemplo. A função está no mesmo código que ela está sendo usada, mas, nada nos impediria de criar um arquivo apenas para separar as funções, assim como fizemos com o HTML com PHP. Criariamos um arquivo chamado funções e usaríamos o comando ***require*** para utilizar a função no nosso código principal.  

Analisando o código acima temos duas variáveis de entrada tipadas como uma string e um número inteiro, as quais receberão o nome e a idade de uma pessoa, consecutivamente.   
Logo abaixo temos a nossa função. Vejamos que para declararmos uma função precisamos colocar o comando ***function***, dar um nome para a nossa função e dentro dos parenteses vamos colocar alguns parâmetros. Fechando isso, vamos tipar o que a nossa função irá retornar. No nosso caso, uma string.  

A função do código acima é para checar a idade de uma pessoa para verificar se ela é autorizada ou não a entrar em um estabelecimento. Então, lemos da seguinte maneira: Se a idade da pessoa for maior ou igual a 18, isso irá nos retornar (*return*) "Welcome in!", caso contrário irá retornar "Sorry! You're not allowed."

Vamos associar essa função a uma variável e então printar ela.  

## **Conclusão**
Caso quisermos reutilizar essa função n vezes para checar a idade em n partes de um código, podemos reutilizar. Esse é o papel básico de uma função e essa é uma das formas que uma função funciona.