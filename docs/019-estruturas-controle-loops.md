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
    echo $i . ", ";
}

echo PHP_EOL . "Script finalizado!";
```

Explicando o bloco de código completo, começamos definindo uma variável com valor igual 10. Após isso, printamos na tela que estaríamos fazendo um script de contagem. Aí sim vamos entrar no nosso laço ```for```.  

No nosso laço podemos perceber que, assim como as condicionais, abrimos parênteses e dentro dele temos a condição que vai fazer o nosso código funcionar, só que aqui ele ficará repetindo de acordo com o que definirmo dentro dos parênteses.  

Como estamos fazendo um script de contagem, usamos índices para indicar a contagem. Por exemplo, no código usamos um ```$i``` para indicar isso. Mas, ainda assim fica confuso com pouca informação.  

Vamos ler da seguinte forma por índices: PARA (for) o nosso contador ($i) começando em 1 e termina em 10 (que foi o número que declaramos na variável), ele vai continuar contando, verificando e vai parar quando o valor for maior que 10. Isto é, ele ainda vai chegar a incrementar o número, vai checar se ele está dentro da condição ```<= 10``` e como é uma condição falsa por não estar dentro do que foi determinado, ele automaticamente para a contagem.  

### **Loop while**
