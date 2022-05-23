# Booleans
Pense em questões que as opções são apenas duas: sim ou não, verdadeiro ou falso etc. Bem, quando falamos em booleans tratamos justamente de valores verdadeiros ou falsos, principalmente.  
Vejamos um exemplo utilizando arrays associativos com booleans.

```php
<?php

$task = [
    'title' => 'Coding homework',
    'due' => 'Tomorrow',
    'completed' => true,
];

var_dump($task) . PHP_EOL;

foreach ($task as $feature => $situation){
    echo "$feature: $situation" . PHP_EOL;
 }
 ```

 Aqui fizemos o mesmo esquema de arrays associativos, printamos nosso array e printamos também algo mais organizado em relação ao array. Se dermos uma analisada na nossa task, podemos ver que a questão se ela completa/se foi feita muda a forma em que está declarada. Isto é devido por ser um valor booleano.  

 Nas linguagens de programação é comum vermos um *true* ou *false* para declarar a situação de algo, e isso é o que chamamos de booleans. Também é comum que esses valores sejam declarados por 0 e 1, mas, antes identificando o que é verdadeiro e o que é falso.