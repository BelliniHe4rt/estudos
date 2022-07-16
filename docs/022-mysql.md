# **Banco de Dados**
Quando armazenamos um dado em uma variável para que algum bloco de código seja executado, nós salvamos temporariamente aquele dado. Caso quisermos que esse dado fique salvo definitivamente, nós utilizamos um banco de dados.  
Um banco de dados é composto por tabelas, que, por sua vez, possuem colunas e, assim, é possível organizar dados de um sistema completo em um banco de dados.  

Além de um banco de dados, também existem os SGBDs, um acrônimo para Sistema Gerenciador de Banco de Dados. Pode-se entender por um Sistema Gerenciador de Banco de Dados como a máquina que estará carregando o banco de dados. Isto é, aqui podemos citar alguns exemplos de bancos de dados comumente utilizados: entre eles estão o SQL, MySQL, MariaDB etc.  

Uma forma de entender como BDs e SGBDs funcionam é colocar na prática e ver o passo a passo deles. Cada máquina serve como o 'gerenciador' de bancos de dados. Por exemplo, caso você queira acessar e manipular um banco de dados pelo terminal, ele irá pedir um usuário, que normalmente é o usuáio que foi utilizado para setar o banco de dados naquela máquina. Mas, quando utilizamos um ```show databases```, ele irá mostrar não apenas um banco de dados criado por você. Caso a máquina for uma máquina compartilhada, ela irá exibir todos os bancos de dados naquele server/máquina.

Aqui iremos ver um um pouco sobre o MySQL, sistema de gerenciamento de b
anco de dados escolhido para estudos e no qual será desenvolvido o processo de estudos para um CRUD.

## **MySQL**
Como vimos, o MySQL é um sistema de gerenciamento de banco de dados. Assim como em desenvolvimento web, em banco de dados também possuímos linguagens diferentes. Aqui, o MySQL é um SGBD que utiliza a linguagem SQL.  
Esse é um dos SGBDs mais conhecidos atualmente.  

Aqui vamos ver o que chamamos de ```query```. Vamos ver as mais utilizadas e também as que compõem meu projeto de estudos (disponível em um repositório no meu perfil, nomeado como ```books-cli```).  
Uma curiosidade antes de partirmos para os códigos é que nas queries do banco de dados vamos sempre enfatizar os comandos, utilizando-os em letra maiúscula.

* ### **Comando SELECT**
O comando SELECT é um comando de busca do MySQL. É um dos comandos básicos, isto é, um dos comandos que está dentro do famoso CRUD (Create, Read, Update, Delete).

Baseado no projeto, podemos utilizar um exemplo.

```sql
SELECT * FROM users; 
```

Basicamente, a query acima está selecionando (ou buscando) tudo da tabela de usuários, o que irá nos retornar todos os items que essa tabela possui e seus respectivos valores.  

* ### **Comando INSERT**
A primeira task do meu projeto foi inserir os dados da tabela de usuários no banco de dados, e para isso utilizei o comando INSERT. Perceptívelmente, esse é um comando de inserção de dados e como exemplo, mais uma vez, vou trazer uma query do projeto.

```sql
INSERT INTO users (name, birthdate, gender) VALUES ('Bellini', '1998-01-01', 'Female');
```

Na query acima inserimos na tabela de usuários o meu nome, minha data de nascimento e meu gênero. Por isso utilizamos o INTO após o INSERT, pois estamos indicando onde vamos inserir aqueles dados.  

* ### **Comando UPDATE**
O comando UPDATE serve para atualizar dados. Com ele utilizamos o comando SET, que serve para podermos inserir quais informações do banco de dados iremos atualizar.

```sql
UPDATE user_books SET devolution_at = CURRENT_TIMESTAMP() WHERE user_id = $userId AND book_id = $bookDevolution;
```

Na query acima (também do meu projeto) estamos atualizando a devolução de um livro. Isto é, ali estamos atualizando da tabela ```user_books``` a data de devolução (utilizando ```CURRENT_TIMESTAMP```), filtrando com WHERE para pegarmos o ID do usuário e do livro.

* ### **Comando DELETE**
O comando DELETE é um daqueles comandos básicos que fazem parte do CRUD, e ele serve para deletar algo no nosso banco de dados. Como exemplo irei utilizar uma query do projeto.

```sql
DELETE FROM users WHERE id = $userID;
```

Na query acima demos uma incrementada nas informações. O que fizemos foi deletar algo direto pelo ID. Então, deletamos da tabela de usuários onde o ID fosse igual ao ID armazenado em uma variável chamada ```userID```.  

Caso quisessemos deletar tudo de uma vez da tabela, poderíamos fazer da seguinte forma (apesar de já termos visto como selecionar tudo):

```sql
DELETE * FROM users;
```

Simples, apenas utilizamos o símbolo * para selecionarmos tudo para que fosse deletado.

* ### **Comando WHERE**
O comando WHERE não nos é desconhecido. Utilizamos esse comando quando fomos deletar algo da tabela de usuários pelo ID. Ou seja, esse comando é um comando de filtragem.

```sql
SELECT * FROM users WHERE id = $userID;
```

Na query acima nós selecionamos tudo da nossa tabela de usuários **onde** o nosso ID fosse igual ao da variável. Ou seja, nós filtramos pelo ID o que queríamos selecionar.

* ### **Comando LIKE**
O comando like pode ser usado para filtragem também, podendo substituir o sinal de **=** na query. Também pode ser visto como um *"autocomplete"* do banco de dados. Ele é utilizado da seguinte maneira.  

```sql
SELECT id, name FROM users WHERE name LIKE '%$userName%';
```

Quando utilizamos o sinal de porcentagem (**%**) no início ou no fim, ou até mesmo em ambas as partes, da variável ou item que queremos filtrar, fazemos aquele esquema de autocomplete que foi dito acima.  

Na query nós selecionamos o ID e o nome de alguém da tabela de usuários onde o nome fosse como o da variável, porém, caso a gente soubesse apenas um nome da pessoa, por exemplo, e precisássemos saber o nome completo, o LIKE e os sinais **%** no início e no fim do que estamos filtrando faria um autocomplete e buscaria nomes que parte deles fossem composto pelo que está na variável.

<!-- ----------------------------------------------------------------------------------------------------
-- Comandos do curso

-- BETWEEN

SELECT * FROM users WHERE birthdate BETWEEN '1998-01-01' AND '2022-01-01';

-- IN

SELECT * FROM users WHERE id IN (5, 10, 15, 20);

-- HAVING

SELECT * FROM users HAVING id = 6;

/*  Funciona como o WHERE, a diferença está na forma de processamento
where = filtra junto com o processamento
having = filtra após o processamento, coisas feitas com base no banco de dados, filtro no pós consulta 
*/

-- ORDER BY

SELECT * FROM users ORDER BY birthdate ASC; -- ASC opcional, com ele ou não será em ordem crescente

SELECT * FROM users ORDER BY birthdate DESC; -- Ordem decrescente

-- LIMIT

/* Se usa depois de todos os comandos na query */

SELECT * FROM users ORDER BY birthdate DESC LIMIT 1,2; -- Busquei por ordem decrescente e pulei o primeiro resultado e escolhi mostrar apenas 2

-- GROUP BY

SELECT COUNT(*) as contagem, faixa_salarial FROM usuarios GROUP BY faixa_salarial;

/* A query acima utiliza o GROUP BY para agrupar informações
O COUNT faz a contagem de quanto de tal coisa possui em cada grupo

Usa-se geralmente em contagens */ -->

<!-- Relacionamento de tabelas

------------------------------------------------------------------
Relacionamento 1:N - Um para muitos;
e.g.: Uma faixa salarial pode "servir" para N usuários

------------------------------------------------------------------
Relacionamento 1:1 - Um par um;
e.g.: Um item está diretamente relacionado a outro item (token, por exemplo)

------------------------------------------------------------------
Relacionamento N:N - Muitos para muitos;
e.g.: Um produto pode ter N cores, uma relação que tem várias opções. Por outro lado uma cor pode estar presente em N produtos diferentes.

 -->

 <!-- Comando JOIN (consulta avançada)

// SELECT usuarios.nome, faixas.titulo FROM usuarios INNER JOIN faixas ON faixas.id = usuarios.faixa_salarial;
- INNER JOIN: relação interna
 
 --> 