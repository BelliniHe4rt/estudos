# **Classes**
Quando falamos de classes, falamos de um nome que pode definir ou classificar qualquer tipo de coisa no nosso projeto.  

***Bellini, como assim? Não entendi.***  
Ok. Vamos usar de exemplos, assim fica mais claro.  

Imagine que temos uma classe nomeada *quarto*. Vamos pensar então o que contém em um quarto: cama, guarda-roupa, cômoda, parede etc. Todo esse conjunto de coisas que classificamos são os atributos de uma classe. Desta forma, vejamos que os atributos de uma classe são o que definem sobre o que ela é, ou o nome da classe define quais atributos ela deve receber.  

``` php
class Quarto
{
    public $cama;
    public $guardaRoupa;
    public $parede;
}
```
Como no exemplo acima, desta forma uma classe seria definida na prática. Nós digitamos *class* e então damos um nome para a nossa classe. Dentro dela (entre chaves) temos seus atributos, que podem ser definidos como público (*public*) ou privado (*private*).  

Em uma classe tem algo que chamamos de métodos, e um dos métodos que são importantes em uma classe é o método construtor. Esse método é declarado através de uma função, como vamos ver em um exemplo. Mas, uma curiosidade interessante sobre os métodos é que eles sempre são uma função dentro da classe.

```php
class Quarto
{
    public function __construct() {

    }
}
```

Esse método construtor será automaticamente instanciado toda vez que uma classe for criada. Mas, para isso precisaremos criar a instância dessa classe.  
Antes de chegarmos lá é importante relembrar um ponto: toda função aceita algum argumento. Isto é, se caso quisessemos passar algum valor na nossa instância, precisaríamos passar esses argumentos no nosso método construtor antes.  

```php
class Quarto
{
    public function __construct($moveis) {
        
        $this->moveis = $moveis;
    }
}

$quarto = new Quarto('Cama', 'Guarda-roupa');
```

// Em estudos, desenvolvimento e falta tirar algumas dúvidas.