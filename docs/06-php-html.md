# PHP e HTML
Quando queremos estilizar uma página web, podemos utilizar HTML e CSS. E aqui veremos como podemos utilizar PHP dentro do HTML para que possamos fazer uma marcação de texto nos nossos dados.    

Antes de sabermos como utilizar o PHP dentro do HTML é preciso saber um pouco sobre HTML. E aqui não irei me estender muito sobre o assunto, uma vez que há um tópico especialmente de HTML aqui. Então, caso haja alguma dúvida sobre, verifique o tópico de HTML antes de prosseguir.  

[Clique aqui para ser redirecionado](/docs/02-html-css.md)  

Prosseguindo, já vimos como funciona o HTML. Mas, e se quisermos usar PHP junto? Ou melhor, e se quisermos estilizar nossos dados em PHP? Bom, vejamos o seguinte exemplo.  

```html
<!DOCTYPE html>
<html lang="pt">

<head>
    <meta charset="UTF-8">
    <title>Tests</title>

    <style>
        header{
            background: purple;
            padding: 2em;
            text-align: center;
        }
    </style>

</head>

<body>

    $name = "Bellini";

    <header>

        <h1>
            <? echo "Hello, $name"; ?>
        </h1>

    </header>
</body>

</html>
```

Acima temos um código no qual implementamos três coisas: HTML, CSS e PHP. Analisando com calma conseguimos identificar cada um deles e decifrar o que estamos fazendo no código.  
Como podemos ver, esse código estaria em um documento HTML, onde, dentro dele, nós colocamos uma estilização com CSS e o nosso PHP. Tudo isso dentro de um código apenas.  

Dentro da tag ```style```. o nosso header está abrigando toda a nossa estilização em CSS da nossa tag ```header```.  
Embaixo, no corpo do documento nós declaramos uma variável com um valor. Após isso, a colocamos em um cabeçalho e printamos com PHP. E aqui é importante analisar e lembrar que se abrimos um código PHP dentro do nosso códig HTML, precisamos abrir e fechar a tag PHP.  Normalmente, quando criamos um documento PHP apenas abrimos a nossa tag PHP no documento. Uma vez que o nosso documento já é declarado que é PHP, não é necessário que fechemos a tag ao fim do código.

## Separando a lógica da estilização
É importante sabermos que quando vamos abrir um documento assim no nosso browser, o primeiro arquivo que ele "enxerga", por assim dizermos, é o arquivo que estiver nomeado com "index". Desta forma, suponhamos que esse código nosso é um *index.tmpl.html*, apenas para colocar a estilização.  

*"Mas, e se quisermos separar esses documentos para termos um apenas para os nossos dados e um para estilizarmos ele?"*  

Bom, aqui é onde vamos conhecer um novo comando chamado *require*.  
Logo acima falamos que o nosso browser irá primeiramente puxar o documento que se chamar *index*, então, no nosso documento index iremos chamar o nosso documento de estilização. Vejamos.

```php
<?php

    $name =  "Bellini";

require 'index.tmpl.php';
```

Aqui podemos analisar que declaramos no nosso index a variável com o valor relacionado a ela. Ou seja, separamos ela da estilização, desta forma, iria ficar apenas o print dela no outro documento junto com o CSS, ficando da seguinte maneira:

```html
<!DOCTYPE html>
<html lang="pt">

<head>
    <meta charset="UTF-8">
    <title>Tests</title>

    <style>
        header{
            background: purple;
            padding: 2em;
            text-align: center;
        }
    </style>

</head>

<body>
    <header>

        <h1>
            <? echo "Hello, $name"; ?>
        </h1>

    </header>
</body>

</html>
```