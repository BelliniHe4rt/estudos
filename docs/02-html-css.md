# **1. O que é HTML?**
  HTML é uma linguagem de marcação de texto usada para carregar e criar páginas na Web. Assim como o Word, comumente usado para criar arquivos de texto e, desta forma, editá-los da maneira mais agradável e facilmente compreensível para o leitor, o HTML consegue fazer as mesmas estilizações em uma página Web (veremos também CSS, um pouco mais tarde).  
  HTML não é uma linguagem de programação, é uma linguagem de marcação de texto, mas, da mesma forma que uma linguagem de programação possui sintaxe e semântica, não é diferente com o HTML. Um documento HTML possui sua própria sintaxe e diferentes formas de indicar o que a parte de um texto quer expressar.    

***"Ok, Bellini... Mas como é essa estrutura/sintaxe do HTML?"***  
Bem, tudo o que queremos colocar em um documento HTML são elementos, e esses elementos sempre estão dentro de tags. Vamos ver um exemplo logo abaixo.


```html
<!DOCTYPE html>
<html>

<head>
	<title>Page Title</title>
</head>

<body>
	<h1>My First Heading</h1>
	<p>My first paragraph.</p>
</body>

</html> 
```

Vamos lá! Para simplificar, quando falamos de tags, falamos de tudo o que está entre os sinais ```<tag>```, assim como vemos no exemplo acima. Sempre que uma tag é utilizada, nós a  abrimos e depois a fechamos, mas, para fechar usamos  a barra, como também podemos ver no exemplo acima, ficando assim:  
```<tag>``` Elemento ```</tag>```.    

Agora, explicando o que cada tag do exemplo acima significa, vamos começar e ir por ordem.

A tag ```<!DOCTYPE html>``` é para reforçar e lembrar o leitor do nosso código que o tipo do nosso documento é um documento HTML. E quando, logo abaixo abrimos a nossa tag ```<html>```, significa que estamos iniciando nosso documento, isto é, essa tag é a raiz do nosso documento HTML. Ou seja, toda as tags dentro e a partir dessa abertura fazem parte do nosso do nosso documento HTML e são tags com sintaxe e semântica próprias da linguagem do nosso código.    

Depois de declararmos o estopim do nosso documento HTML temos a tag ```<head>```, a qual vai ter as informações gerais sobre a nossa página HTML, como, por exemplo próprio, o ```<title>``` que está dentro da nossa tag. A tag ```<title>``` indica o título da nossa página HTML. Podemos identifica-la na barra onde a página está sendo exibida. Lembrando, sempre que uma tag é ```<aberta>```, ela precisa ser ```</fechada>```.  

Saindo das informações gerais vemos a tag ```<body>```, a qual indica, como o próprio nome já diz, o corpo do nosso documento. Isto é, a maior parte do que formos fazer na nossa página estará dentro da tag ```<body>```. Assim, temos como exemplo duas "ações" sendo declaradas dentro da nossa tag, sendo elas a tag ```<h1>``` e a tag ```<p>```.  

***"Mas, Bellini, o que significa essas tags?"***  
Bom, é aqui onde começa todo o conteúdo da nossa página em si e vamos visualizar isso através das tags. Como os próprios elementos no exemplo mostram, a tag ```<h1>``` indica que o elemento dessa tag é um tipo de cabeçalho. Claro, esse cabeçalho pode conter diversos tamanhos onde a tag iria variar entre seus números. Por exemplo, poderíamos usar de ```<h2></h2>``` até ```<h6></h6>```, mas, o que se diferencia nessas tags não é só o tamanho. Aqui vamos falar um pouco de semântica! Quando usamos o ```<h1>``` para indicar um cabeçalho, queremos dizer para o leitor do nosso código que aquele é o cabeçalho principal da nossa página, e os outros cabeçalhos são de importância secundária em relação ao nosso ```<h1>```.  

Essa questão de semântica não veremos apenas com a tag do nosso cabeçalho, mas, em outras tags que compõem o HTML. E isso é um ponto importantíssimo, pois é o que vai tornar o código legível para quem estiver lendo. Ou seja, quanto mais semântica usarmos no nosso código, mais legível ele será.  

Ok, mas ainda temos a nossa tag ```<p>``` para falar sobre. Essa tag não é nada mais do que um parágrafo. Vamos adotar esse olhar sobre as tags, do que elas são e não o que elas indicam, pois quando olharmos para uma página será mais fácil lê-las e interpretá-las com essa visão. Saberemos o que é um cabeçalho e o que é um parágrafo, saberemos o que é o título da página.

## **1.1. Tags HTML**
Aqui veremos um pouco mais sobre outras tags HTML, conhecê-las e tratar um pouco de semântica em algumas delas.    

* ### Link  
Essa é uma tag na qual usamos atributos, isto é, uma estrutura onde vamos encontrar uma chave e um valor para essa chave **(key=value)** dentro e após ter nossa tag de link ```<a> ```, por exemplo:  

```html
<!DOCTYPE html>
<html>
	<body>
		<a href="https://google.com">Você está fazendo um link para o Google.</a>	
	</body>
</html> 
```  
O que fizemos acima foi criar um link no qual clicando nos elementos da nossa tag, seríamos redirecionados ao Google, usando o atributo ***href*** e como valor dele a URL do Google.  

* ### Imagem
Para adicionarmos uma imagem a nossa página usaremos a tag ```<img>```, sendo essa também uma tag na qual usamos atributos. Atributos esses que são usados para definir a origem da imagem (src), sua largura (width) e sua altura (height), e também podemos colocar um texto alternativo (alt). Dessa forma, a sintaxe para adicionarmos uma imagem ficaria ca seguinte maneira:

```html
<!DOCTYPE html>
<html>
	<body>	
		<img src="origem.jpg" alt="texto alternativo" width="150" height="150">	
	</body>
</html> 
 ```  

 * ### Quebra de linha
 Para quebrarmos uma linha em HTML nós usamos a tag ```<br>```, que significa *break row* em inglês, isto é, nosso "quebrar linha". Uma curiosidade desta tag é que não precisamos abrir e fechar, ela é usada normalmente aberta. Vejamos um exemplo:

 ```html
<!DOCTYPE html>
<html>
	<body>	
		<p>Isto é um parágrafo.</p><br>
		<p>Isto é outro parágrafo.</p>
	</body>
</html>
```

## **1.2. Estilização em HTML**  

Como dito, com HTML conseguimos editar um documento da mesma forma que editamos um pelo Word. Aqui vamos ver um pouco das formas de estilizar nosso documento HTML.

### **Style**
Para estilizarmos nosso documento usaremos do atributo ```style``` dentro da nossa tag. Ou seja, utilizaremos a tag normalmente, assim como vimos antes no exemplo de links, e colocar o atributo com seus valores logo após a tag ser declarada. Vamos ver aqui como fica e como podemos fazer essas alterações em cada elemento específico.

* ### Cor do background
Para mudarmos qualquer elemento pelo atributo ```style```, vamos precisar de uma propriedade e um valor que são parte do CSS para definirmos essa estilização, isso com qualquer tag e qualquer forma de estilização. Nesse caso aqui, ficaria da seguinte maneira.

```html
<!DOCTYPE html>
<html>
	<body>	
		<p style="background-color:powderblue;">
			Isto é um parágrafo com uma cor de fundo.
		</p>	
	</body>
</html>
```

O que vemos de diferente na forma de utilização do nosso atributo é que seu valor também possui um valor. Isto é, precisamos definir o que queremos estilizar e de que forma queremos que seja estilizado. Aqui vemos que queríamos mudar a cor de fundo e depois de ```:``` definimos a cor que queríamos (cores essas que também poderiam ser definidas em hexadecimal).

* ### Cor do texto
Vimos que para mudar a cor de fundo do nosso elemento utilizamos um atributo, aqui faremos a mesma coisa, apenas iremos mudar o valor do atributo. Quando falamos de valor do atributo, vale lembrar que esses valores são relacionados ao CSS como propriedade e valor da propriedade.  
Para mudar a cor do texto, vamos apenas indicar a propriedade ```color``` e depois o mesma esquema de indicar a cor. Vai ficar da seguinte forma:

```html
<!DOCTYPE html>
<html>
	<body>	
		<p style="color:red;">Isto é um parágrafo com a cor do texto modificada.</p>	
	</body>
</html>
```

* ### Fonte
Para mudarmos a fonte vamos fazer o mesmo processo de estilização, vamos apenas mudar a nossa propriedade. Desta forma, ficaria com a seguinte sintaxe:

```html
<!DOCTYPE html>
<html>
	<body>	
		<p style="font-family:verdana;">Isto é um parágrafo com a fonte Verdana.</p>	
	</body>
</html>
```  
  
Relembrando, sempre que formos usar o atributo ```style```, iremos precisar que seu valor seja uma propriedade com o valor dela, sempre referenciando o que queremos mudar e como queremos queremos mudar.

* ### Tamanho do texto
Fácil como mudar a cor do nosso texto ou a sua fonte, faremos o mesmo com o seu tamanho, indicando o tamanho com ```font-size```, o qual pode ser apontado em pixels ou porcentagem. Vamos ver como ficaria:

```html
<!DOCTYPE html>
<html>
	<body>	
		<p style="font-size:150%;">Isto é um parágrafo com a fonte em 300%.</p>	
	</body>
</html>
```

* ### Alinhamento do texto
Para mudar o alinhamento do nosso texto vamos seguir a mesma sintaxe também, mudando apenas as propriedades e valor do atributo, que aqui são ```text-align```, e podemos escolher assim qual o alinhamento do texto. Assim:

```html
<!DOCTYPE html>
<html>
	<body>	
		<p style="text-align:center;">Este é um texto centralizado.</p>	
	</body>
</html>
```

### **Formatando elementos**
Aqui iremos voltar para as tags e vamos falar um pouco daquela tal semântica mais uma vez.  
A semântica nada mais é do que a forma de como damos importância para algo em um código. Por exemplo, aqui vamos ver algumas tags diferentes que possuem a mesma função, e o motivo delas serem diferentes é a semântica; ou seja, uma tag que tem tal função pode ser diferente da outra tag com a mesma função por questões de importância, de deixar o código cada vez mais legível para o leitor.  
Quando falamos de de deixar o código legível e semântica, queremos expressar justamente o quão fácil está de identificar a importância e intensidade de cada tag dentro de sua função. Vejamos algumas dessas tags:  

* ### Negrito
Para deixar o texto em negrito no HTML existe duas tags: ```<b>```, de *bold*, e `<strong>`. As duas tags possuem a mesma função e vamos testar isso; o que diferencia uma tag da outra é a tal da semântica. Se quisermos expressar no nosso código que aquele negrito tem certa importância ali, usaremos o ```<strong>```, caso o texto não tenha tanta importância e seja mais uma questão de estilo mesmo, podemos usar o ```<b>```.

```html
<!DOCTYPE html>
<html>
	<body>	
		<p><b>Este texto está em negrito.</b></p>
		<p><strong>Este texto está em negrito também.</strong></p>	
	</body>
</html>
```

Como podemos ver, temos duas tags diferentes que possuem funções iguais. Isso porque temos a semântica!

* ### Itálico
Assim como em negrito temos formas diferentes de expressar a mesma ideia, em itálico também temos essas opções semânticas para definir no nosso código qual texto em itálico é o mais relevante. Vejamos;

```html
<!DOCTYPE html>
<html>
	<body>	
		<p><i>Este texto está em itálico.</i></p>
		<p><em>Este texto está em itálico também.</em></p>	
	</body>
</html>
```

* ### Small
Para deixarmos um texto pequeno, usamos a tag ```<small>```. Isso fará com que o nosso elemento fique <small>menor</small>. Vejamos:

```html
<!DOCTYPE html>
<html>
	<body>
		<p><small>Este texto está em pequeno.</small></p>	
	</body>
</html>
```

* ### Marca texto
Para passarmos uma marcação em cima de um elemento, usamos a tag ```<mark>```, a qual <mark>marcará</mark> da forma padrão o nosso texto. Vamos ver sua sintaxe:

```html
<!DOCTYPE html>
<html>
	<body>	
		<p><mark>Este texto está marcado.</mark></p>
	</body>
</html>
```

## **2. CSS**
Com o HTML vimos diversas maneiras de editarmos um texto diretamente pela tag. Mas, e se quisermos fazermos um documento para essas estilizações?  
Bom, é aí que entra o CSS! Para termos um código mais organizado e bonito.    

Para o início disso tudo, precisaremos criar um documento ```.css``` (Por exemplo, style.css) para guardar a nossa estilização e puxarmos uma *request* para dentro do nosso documento ```.html``` depois.    

*"Nossa, Bellini... Que complicado!"*  
Não é, não. Vamos lá dar uma espiada na sintaxe...

```html
<!DOCTYPE html>
<html>
	<head>
		<link rel="stylesheet" href="styles.css">
	</head>
</html>
```

Se lembram que na tag ```<head>``` colocamos todas as informações gerais do nosso código? Bem, o que fizemos nesse código foi uma referência ao nosso documento ```.css```, puxando todas as formatações dele para dentro do nosso documento HTML. Agora podemos utilizar nosso documento ```.css``` para fazer nossa estilização.    

Ok, para fazermos estilização em CSS vamos utilizar classes e IDs dentro da nossa tag no documento html e depois utilizar o nome dessa classe no documento CSS. No documento CSS ficaria algo parecido com o que vamos ver agora.

```css
body {
  background-color: powderblue;
}
h1 {
  color: blue;
}
p {
  color: red;
}
```

Aqui alteramos o background de toda a nossa tag ```<body>``` e as cores de texto do nosso cabeçalho e parágrafo.  
Outra coisa que podemos fazer com CSS é adicionar um espaço para fora ou dentro da margem do nosso elemento usando ```margin``` e ```padding```. Para ambos precisamos definir também o tamanho da nossa borda (com o ```border```) para que possamos visualizar melhor nosso espaçamento. Não é uma regra, mas, se quisermos visualizar como nosso código está agindo, é uma boa ideia.   

* ### Margin
Margin define um espaço para fora da sua borda para ser espaçado, podendo ser indicado em pixel, porcentagem...  
Sua sintaxe ficaria da seguinte forma:

```css
p {
  border: 2px solid powderblue;
  margin: 50px;
}
```

Aqui definimos o tamanho da nossa borda para 2 pixels e sua cor para powderblue, e o espaçamento para **fora** da nossa borda para 50 pixels.


* ### Padding
Ao contrário do ```margin```, o ```padding``` já mostra esse espaçamento para o lado de dentro da nossa borda. Essa é a única diferença entre um e o outro. Na sintaxe do exemplo acima, mudaríamos apenas de margin para padding e no elemento seria espaçado de uma forma totalmente diferente.

```css
p {
  border: 2px solid powderblue;
  padding: 50px;
}
```

Aqui definimos o tamanho da nossa borda para 2 pixels e sua cor para powderblue, e o espaçamento para **dentro** da nossa borda para 50 pixels.    

## **Conclusão**
Bom, aqui aprendemos o básico sobre HTML e CSS e só com esse básico podemos fazer páginas e páginas na Web, conseguimos ler um site sabendo o que cada item dele é dentro do HTML e do CSS... Conhecimento que sempre se expande.  
Agora é só sair por aí vasculhando sites e testando, quem sabe, fazer uma página especialmente sua.