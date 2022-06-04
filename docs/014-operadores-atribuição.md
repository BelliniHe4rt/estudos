# Operadores de atribuição
Quando falamos de *atribuir* algo, logo se dá a entender que estamos referenciar algo em algum lugar.
Vejamos alguns exemplos para entender melhor.  

## **Atribuindo valores a uma variável**  
Para atribuírmos um valor a uma variável, utilizamos o sinal de igual (**=**).

```php
<?php

$numero = 5;
```

Isto é, ao atribuírmos um valor, estou declarando/dando um valor a algo.

## **Atribuições abreviadas**
Temos como abreviar algumas atribuições usando <a href="/docs/012-operadores-aritmeticos.md">valores aritméticos.</a> Vejamos alguns exemplos com eles.  

* **Adição**  
Para fazermos uma soma direta, sem utilizar duas variáveis, podemos atribuir o valor da soma diretamente na variável, fazendo com que seu valor seja alterado.

```php
<?php

$numero = 5;
$numero +=5;
```

No exemplo acima, a variável passou a valer 10, porque após ela ser declarada valendo 5, foi atribuído a ela a soma de +5.

* **Subtração**  
O mesmo da soma serve aqui para a subtração e o mesmo para as outras operações aritméticas.  

```php
<?php

$numero = 5;
$numero -=2;
```

No exemplo, a variável que valia 5 passou a valer 3, uma vez que foi subtraído 2 dela.  

* **Multiplicação**  
Na multiplicação faremos o mesmo que fizemos com as outras operações.  

```php
<?php

$numero = 5;
$numero *=5;
```

Aqui a variável *numero* passou a valer 25, uma vez que foi atrubuída a ela a multiplicação por 5 vezes o seu valor.  

* **Divisão**  
Para dividirmos uma variável de forma abreviada também não muda a forma em que é feito.

```php
<?php

$numero = 10;
$numero /= 5;
```

Acima, o valor da nossa variável passou a ser 2, já que ela foi dividida por 5 quando valia 10.

* **Resto de uma divisão (Módulo)**  
O resto de uma divisão, chamado de módulo, pode ser obtido através de uma operação de atribuição também, ficando da seguinte maneira.

```php
<?php

$numero = 10;
$numero %= 5;
``` 

Aqui o retorno da nossa operação seria igual a zero, já que o resto (o resto, não o resultado) da divisão do nosso número por 5 seria igual a zero.

## **Curiosidades**
No PHP conseguimos incrementar e decrementar valores. Bem, os operadores de incremento e decremento são declarados diretamente com a variável.  
Para incrementarmos um valor (o que será +1) a uma variável, podemos fazê-lo das seguintes formas.

```php
<?php

$numero = 5;

++$numero; // Aqui a variável passou a valer 6
$numero++; // Aqui a variável continua valendo 6
```

Como está acima, podemos incrementar a uma variável usando ***++*** antes ou depois de declarar a variável. O mesmo serve para o decremento, sendo usado o sinal ***--*** no lugar.  

Mas, por que a variável que foi incrementada antes funcionou e a outra não?  
Bem, em tese ambas funcionaram. O motivo da segunda não ter mudado o valor é porque a variável não foi declarada novamente depois, já que o incremento foi feito após a variável ter sido declarada. Ou seja, para o seu valor ser alterado, deveria ter sido declarada novamente, da seguinte maneira.

```php
<?php

$numero = 5;

++$numero; // Aqui a variável passou a valer 6
$numero++; // Aqui a variável continua valendo 6

$numero; //Agora a variável vale 7
```
