# Comparação de valores
Como em outros artigos eu já disse que algumas coisas na computação poderíamos comparar com o que aprendemos na escola para facilitar, nesse tópico também não será diferente.  

Quando aprendemos a comparar na escola, começamos pela língua portuguesa, a qual nos apresentou duas palavras interessantes: **antônimos** e **sinônimos**. Para antônimos entendemos o que é diferente ou, melhor, o contrário de algo. Já para sinônimos entendemos algo que tem alguma semelhança.  

Como na computação trabalhamos muitas vezes com <a href="/docs/08-booleans.md">booleanos</a>, que são valores opostos correspondentes a 1 ou 0, também conhecidos como *true* (verdadeiro) ou *false* (falso), aqui veremos alguns operadores para fazer comparação de valores.

* **Igualdade**  
Quando queremos saber se um valor é igual a outro valor, os comparamos utilizando **==**. Desta forma nos será retornado se a comparação é verdadeira ou falsa. Vejamos um exemplo.

```php
<?php

echo (0 == false) . PHP_EOL; //true
echo (1 == true) . PHP_EOL; //true
echo ('numero' == 10) . PHP_EOL; //false
```

* **Diferença**  
Para testarmos se um valor é diferente de outro valor utilizamos o operador **!=**, então, caso o valor seja diferente nos será retornado *true* e caso o valor seja igual será retornado *false*.

```php
<?php

echo (0 != false) . PHP_EOL; //false
echo (1 != true) . PHP_EOL; //false
echo ('numero' != 10) . PHP_EOL; //true
```

* **Idêntico**  
O operador de idêntico (**===**) verifica se os valores testados são do mesmo tipo. Por exemplo...

```php
<?php

echo (0 === false) . PHP_EOL; //false
echo (1 === true) . PHP_EOL; //false
echo ('numero' === 10) . PHP_EOL; //false
```

* **Não idêntico**  
O operador de  idêntico (**!==**) verifica se os valores testados não são do mesmo tipo. Basicamente faz o contrário do operador idêntico.

```php
<?php

echo (0 !== false) . PHP_EOL; //true
echo (1 !== true) . PHP_EOL; //true
echo ('numero' !== 10) . PHP_EOL; //true
```

* **Maior e menor**  
Na matemática aprendemos a usar os sinais de maior (**>**) e menor (**<**), bem como podemos usar maior ou igual (**>=**) e menor ou igual (**<=**). Vamos ver nos exemplos.

```php
<?php

echo (1 < 2) . PHP_EOL; //true
echo (1 > 2) . PHP_EOL; //false
echo (1 <= 2) . PHP_EOL; //true
echo (1 >= 2) . PHP_EOL; //false
```
