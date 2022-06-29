# **Estruturas de controle**
As estruturas de controle são parte de um código que é executado com base em algum teste lógico. Existem vários tipos de estruturas controle utilizadas para tomar uma decisão e nesse tópico vamos tratar apenas dos **loops**.

## **Loops**
Os loops são estruturas de controle baseadas em repetições, isto é, uma parte do código é repetida dentro de certa condição. Sim, aqui também usaremos as condicionais de certa forma para executar os loops.  

Em um outro ponto de vista, da mesma forma que as condicionais executam um teste lógico para verificar e executar o que for verdadeiro, aqui os loops fazem a mesma coisa. Enquanto a condição que estiver dentro do nosso loop for verdadeira, ele continuará repetindo até que acabe aquele bloco de código ou se torne falso.  

### **Loop for**
Antes de falarmos sobre o laço de repetição ```for```, vamos entender algumas expressões que vamos usar a partir daqui. São essas expressões: **argumentos** e **parâmetros**.

Para parâmetros podemos checar a definição da palavra em português, onde, em uma função, são as informações que a gente vai receber.  
Já para os argumentos, são a forma que desejamos executar a função.

*Em outras palavras e deixando mais fácil: quando você argumentando, ou seja, provando algo para afirmar alguma coisa, você está passando algo, ou seja, na programação você está passando valores (argumentos) para alguma função receber (parâmetros).*

Mas, vejamos um exemplo para saber o que são esses tais argumentos e parâmetros.

```php
<?php

$contador = 10;

echo "Script pra contar até $contador" .PHP_EOL;

for($i = 1; $i <= $contador; $i++){
    echo $i . ', ';
}

echo PHP_EOL . "Script finalizado!";
```

Explicando o bloco de código completo, começamos definindo uma variável com valor igual 10. Após isso, printamos na tela que estaríamos fazendo um script de contagem. Aí sim vamos entrar no nosso laço ```for```.  

No nosso laço podemos perceber que, assim como as condicionais, abrimos parênteses e dentro dele temos a condição que vai fazer o nosso código funcionar, só que aqui ele ficará repetindo de acordo com o que definirmo dentro dos parênteses.  

Como estamos fazendo um script de contagem, usamos índices para indicar a contagem. Por exemplo, no código usamos um ```$i``` para indicar isso. Mas, ainda assim fica confuso com pouca informação.  

Vamos ler da seguinte forma por índices: PARA (for) o nosso contador ($i) começando em 1 e termina em 10 (que foi o número que declaramos na variável), ele vai continuar contando, verificando e vai parar quando o valor for maior que 10. Isto é, ele ainda vai chegar a incrementar o número, vai checar se ele está dentro da condição ```<= 10``` e como é uma condição falsa por não estar dentro do que foi determinado, ele automaticamente para a contagem.  

### **Loop while**
Como vimos, as estrtuturas de controle utilizam condicionais também, isto é, uma operação booleana para verificar um teste lógico; e a estrutura de controle do loop while trabalha com uma condição que enquanto for verdadeira fará com que o nosso loop seja executado. Em outras palavras, o nosso loop while só possui uma condição verdadeira no teste lógico e continua sendo executado até que o resultado do teste seja falso.  

Vejamos um bloco de código que executa a mesma função do código do loop for para entendermos melhor.  

```php
<?php

$condicaoLoop = true;
$contador;

echo "Script pra contar até $contador" .PHP_EOL;

while ($condicaoLoop){
    echo $contador . ', ';
    if ($i == 10){
        $condicaoLoop = false;
    }
    $contador++;
}

echo PHP_EOL . "Script finalizado!";
```

Ok... No bloco de código acima fizemos o mesmo procedimento da contagem até o número 10, mas, aqui usando o loop while. O loop while utilizou mais linhas de código do que o loop for. Nesses casos em que vamos incrementar algo, o loop for é mais útil do que o loop for, não por questões de funcionamento, pois ambos exercem a mesma tarefa sem problemas.  

### **Loop foreach**
O loop foreach não nos é desconhecido. Quando estudamos sobre arrays nós vimos esse loop lá, então já sabemos que o loop foreach é utilizado juntamente com arrays.  
Este loop é utilizado para iterar arrays e como exemplo podemos até mesmo ver algum bloco de código de quando estudamos arrays.  

```php
$task = [
    'title' => fgets(STDIN),
    'due' => fgets(STDIN),
    'completed' => fgets(STDIN),
];

var_dump($task) . PHP_EOL;

foreach ($task as $feature => $situation){
    echo "$feature: $situation" . PHP_EOL;
 } 
```  

O bloco de código acima também nos é conhecido, mas, para reforçar, vamos tentar endende-lo mais uma vez.  
Nós temos um array que armazena as nossa tarefas, as quais possuem um título, uma data para entrega e um status para ver se ele está completo ou não. Quando passamos o nosso array associativo pelo foreach, colocamos dentro da condição do nosso loop que para cada item da nossa task contando como chave => valor, nós iríamos printar a chave e o valor de acordo com o que está dentro do nosso echo.  

## **Controle de repetições**
Muito além de acharmos que nossos loops trabalham apenas de acordo com a condição que damos no início dele, podemos controlar suas repetições com os comandos ```continue``` e o comando ```break```.

* **Continue**  
O comando *continue* 