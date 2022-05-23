# Conditionals
Suponhamos que ao irmos ao mercado queremos comprar um produto e temos apenas R$10.00. Nesse caso, teríamos uma condição. Se o valor do produto for menor ou igual a R$10.00, podemos comprar o produto; caso contrário, não podemos efetuar a compra.  

Trazendo isso para o exemplo de tasks que estamos seguindo, vamos analisar o seguinte exemplo.

```php
<?php

$task = [
    'title' => 'Coding homework',
    'due' => 'Tomorrow',
    'completed' => false,
];

var_dump($task) . PHP_EOL;

foreach ($task as $feature => $situation){
    echo "$feature: $situation" . PHP_EOL;
 }
     if ($task['completed'] = true) {
        echo "Complete";
    }else {
        echo "Incomplete";
    }
 ```

Aqui, mais uma vez, temos o nosso array printado com o *var_dump* e com o *foreach* organizando ele em tópicos com chave e valor. Agora temos um novo comando, que é o *if* e o *else*.  
Esses comandos são responsáveis para decidir como uma condição deve agir. Vejamos.  

No nosso código vemos que **se** o tópico *completed* da nossa task for igual a *true*, então devemos printar que ela está completa, **senão** iremos printar que ela está incompleta.  

P.S.: Quando temos mais de uma opção verdadeira na nossa condição, podemos usar o ***else if*** para declarar todas as opções que podem ser verdadeiras.