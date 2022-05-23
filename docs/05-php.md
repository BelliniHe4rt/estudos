# PHP
Em algum momento dos nossos estudos precisamos focar em alguma linguagem de programação, isso nos ajudará a ter mais noção do que queremos para o nosso futuro, em qual área queremos trabalhar.
O PHP é uma linguagem de programação server side, e uma linguagem surpreendente para desenvolver páginas web.  Aqui irei estudar um pouco de sua sintaxe e como desenvolver com PHP.  

## Variáveis
As variáveis são um meio de armazenar algum dado em PHP. E para isso sempre precisamos atribuir um nome a essa variável, o que é muito importante, pois o nome da variável indica o que ela é. Como desenvolvedores devemos pensar muito sobre isso, pois é o que deixa nosso código mais limpo também.  
Para declarar uma variável em PHP colocamos um cifrão ($)    e o nome da nossa variável, finalizando com um ponto e vírgula (;), assim:  

```php
$nome = Bellini;
```

Até então, apenas criamos uma variável que guarda o nome Bellini. Podemos ver isso na nossa tela utilizando o comando *echo*.

```php
echo "Olá, meu nome é $nome";
```

O comando *echo* nos permite printar algo na tela. É um comando de saída de dados.  
E assim entraram algumas coisas novas para analisarmos, como as aspas e a variável dentro dela.  Vejamos que essas aspas são duplas, o que aparenta-nos que estamos printando uma string e uma variável dentro dela. Caso fossem aspas simples isso não teria sido possível, e iríamos precisar fazer uma concatenação. Exemplo:

```php
echo 'Olá, meu nome é' . $name . PHP_EOL;
```

Aqui concatenamos a nossa string à nossa variável utilizando um ponto, e da mesma maneira concatenamos um PHP_EOL no fim. Esse último "comando" significa PHP End Of Line, que aponta que chegamos ao fim da linha, desta forma avançando para a próxima linha.