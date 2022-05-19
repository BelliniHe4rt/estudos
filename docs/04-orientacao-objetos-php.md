# **1. Orientação a Objetos** 
Primeiramente, antes de entrarmos nos aspectos que nos mostrarão como programar algo orientado a objetos, precisamos saber o que é esse tal de POO.   
Hoje em dia muitas linguagens de programação utilizam o conceito de orientação a objetos, sendo as mais conhecidas como o C#, C++, Java e Python, por exemplo. Aqui nós iremos estudar orientação em objetos em PHP.   

*Mas existe orientação em objetos em PHP?*  
Pois é, na faculdade o que eu mais ouvia era julgamentos em relação ao PHP e sempre a mesma frase repetida: *"PHP nem é orientado a objetos!*. Bem, aqui veremos o contrário. Orientação a objetos é um paradigma adotado por várias linguagens de programação onde o programa (ou podemos dizer que a própria orientação a objetos) é formado(a) por dados e comportamentos.   

Então, vamos checar um pouco do que compõe a orientação a objetos.   

## **Classes** 
Vejamos que para formarmos classes nós temos que classificar algo, então dentro dessa classe nós teremos o que chamamos de atributos da classe. Por exemplo, se formos classificar uma casa veremos o tamanho do terreno, quantos cômodos essa casa tem etc. Todas essas informações da nossa casa são os atributos dela.  
Ou seja, dentro de uma classe, nós teremos os atributos dela, que são informações que definem do que ela é composta e como ela é. Vejamos um exemplo:  

``` php
class Task
{
    public $title;
    public $description;
    public $due;
}
```

Bem, analisando o exemplo acima nós podemos ver que criamos uma classe para uma tarefa e atribuímos a essa tarefa um título, uma descrição e um prazo para entrega.  Isso é o básico de uma classe.

## **Objetos**
No exemplo acima (das classes) vimos que nós atribuímos alguns valores a ela, e esses valores são chamados de atributos ou objetos. Ou seja, nosso objeto sempre será informações atribuídas a classe. Por exemplo:

``` php
class Person
{
    public string $name;
    public int $age;
    private string $address;
}
```

Quando olhamos para a nossa classe que se refere a uma pessoa, vemos que atribuímos um nome, idade e um endereço para essa pessoa. Esses são os objetos da nossa classe. Aqui ainda acrescentamos um pouco mais de informação, que são os tipos desses objetos, e encontramos duas *strings* e um *int*.  
Outra coisa que podemos perceber nesse exemplo é que um dos nossos dados é privado! Quando algum dado está em *private*, significa que esse dado só pode ser acessado de dentro da nossa classe.

## **Herança**
Quando queremos que uma outra classe do nosso código possua o mesmo comportamento de outra classe, nós usamos herança para isso. A herança é o que facilita essa adoção de comportamento, sem precisar que parte da classe seja escrita novamente dentro de outra classe, sendo que podemos simplesmente adotar aquela partezinha do código com o comando *extends*.  