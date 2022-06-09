# **Operadores de execução**
Os operadores de execução são utilizados para executar um comando do terminal pelo código utilizando as aspas invertidas, ou backquotes em inglês. Isto é, utilizando ``` `` ``` podemos executar comandos a nível de terminal utilizando aspas invertidas.  

```php
<?php

$output = `ls -al`;
echo "<pre>$output</pre>";
```

O comando dentro das aspas invertidas é equivalente a uma listagem completa do que há dentro do nosso repositório.