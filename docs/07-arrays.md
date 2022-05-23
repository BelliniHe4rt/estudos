# Arrays
Quando vimos sobre PHP, logo falamos das variáveis. Uma variável é uma capaz de armazenar um valor, já um array é capaz armazenar mais de um valor. Por exemplo, se quisermos fazer uma lista de animais apenas com variáveis, ficaria da seguinte maneira:

```php
<?php

    $animal1 = "Borboleta";
    $animal2 = "Morcego";
```

A questão de um array é que ele pode armazenar vários valores. Ou seja, se quisermos refazer essa lista de forma mais fácil e que deixaria o código limpo e bonito, faremos da seguinte forma:

```php
<?php

    $animais = [
        'Borboleta',
        'Cachorro',
        'Morcego',
    ];
```

Um outro ponto sobre arrays é que para printar o nosso array na tela nós podemos, claro, usar o comando *echo*. Mas, o mais indicado para se fazer essa ação é utilizar o comando *var_dump*, sendo sua sintaxe a seguinte.

```php
<?php

    var_dump($array) . PHP_EOL;
```

Sabendo o básico sobre arrays, podemos entender um pouco sobre arrays associativos.

## Arrays associativos
Utilizamos arrays associativos quando queremos atribuir um valor a algum dado de dentro do nosso array. Vejamos um exemplo com alguma task.

```php
$task = [
    'title' => $argv[1],
    'due' => $argv[2],
    'completed' => $argv[3],
];

var_dump($task) . PHP_EOL;
```

Quando rodamos nosso código, podemos passar os dados através de argumentos.  
*Mas o que isso significa?*  
Bem, após colocarmos o nosso comando para rodar o código, nós colocamos valores que serão relacionados ao *argv*. O ponto aqui é ele vai pegar um valor por vez.  

Se quisermos pegar o valor por linha, podemos usar um comando diferente, o *fgets*. Ficaria da seguinte maneira:  

```php
$task = [
    'title' => fgets(STDIN),
    'due' => fgets(STDIN),
    'completed' => fgets(STDIN),
];

var_dump($task) . PHP_EOL;
```

Se quisermos também printar o nosso array passando por cada um deles colocando como se fossem em tópicos, podemos usar o comando *foreach*. Vejamos.

```php
foreach ($task as $feature => $situation){
    echo "$feature: $situation" . PHP_EOL;
 } 
 ```

Aqui nós determinamos que, para cada item da nossa task contando como *chave => valor*, nós iríamos printar a chave e o valor de acordo com o que está dentro do nosso *echo*.  
Desta forma, tudo que estiver antes do sinal " => " é a nossa chave, e o que estiver depois é o nosso valor.