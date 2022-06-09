# **Operadores lógicos**
Os operadores lógicos tratam-se se operadores que trabalham com valores booleanos. Desta forma, antes de realizar uma operação utilizando o valor, ele é convertido para booleano.  

Aqui veremos quais são esses operadores lógicos e como eles funcionam.  

* **Operador E (```&&``` ou ```and```)**  
O operador **E** é operador verdadeiro, ou seja, se ambos os valores no qual ele estiver operando forem verdadeiro, irá nos retornar ```true```.  

```php
<?php

$a = 1;
$b = 1;

if($a && $b == 1) {
    echo true;
}

endif;
```  
  
* **Operador OU (```||``` ou ```or```)**  
Diferente do operador **E**, o operador **OU** nos retorna ```true``` quando um dos valores que estão sendo operados for verdadeiro.

```php
<?php

$a = 1;
$b = 2;

if($a || $b == 1) {
    echo true;
}

endif;
``` 
  
* **Operador XOR (```^``` ou ```xor```)**  
Esse operador é conhecido como um **OU exclusivo**, e ele nos retorna ```true``` quando um dos valores que estão sendo operados forem verdadeiros também. A diferença é que ele não retornará ```true``` se ambos os valores forem verdadeiros.

```php
<?php

$a = 1;
$b = 1;

if($a ^ $b == 1) {
    echo false;
}

endif;
```  

Aqui o nosso retorno foi falso, pois ambos os valores são verdadeiros.  


* **Operador NÃO (```!``` ou ```not```)**  
O operador **NÃO** nega o valor que está sendo operado. Ou seja, negando um valor booleano temos o contrário. Se negarmos um ```true``` nos será retornado ```false``` e se negarmos um ```false``` nos será retornado ```true```.

```php
<?php

$a = false;

var_dump(!$a);

endif;
```