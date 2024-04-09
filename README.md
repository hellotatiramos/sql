

<div align="center">
<img src="https://github.com/hellotatiramos/sql/assets/158481113/e6e14496-a22f-41a6-80a2-467e5a51968f" width="300px" />
</div>



## O que é SQL? 
>*SQL (Structured Query Language) é uma linguagem de programação utilizada para interagir com bancos de dados. Ela permite que você faça coisas como criar, modificar e consultar informações em um banco de dados. Pense nela como uma linguagem que você usa para falar com o banco de dados e pedir a ele que faça coisas por você, como encontrar dados específicos, adicionar novos dados ou alterar dados existentes. É uma ferramenta fundamental para trabalhar com dados de forma eficiente e organizada.*

## Cláusulas 

>*As cláusulas SQL são elementos fundamentais usados para consultar e manipular dados em um banco de dados relacional. Aqui estão algumas das principais cláusulas SQL:*

`SELECT`: Utilizada para selecionar dados de uma ou mais tabelas.

`FROM`: Especifica a tabela ou tabelas das quais você está selecionando os dados.

`WHERE`: Permite filtrar os registros com base em uma condição especificada.

`GROUP BY`: Agrupa registros com base em uma ou mais colunas e permite que funções agregadas, como SUM, AVG, COUNT, etc., sejam aplicadas a cada grupo.

`HAVING`: Funciona de maneira semelhante à cláusula WHERE, mas é usada para filtrar grupos resultantes de uma cláusula GROUP BY com base em condições específicas.

`ORDER BY`: Ordena os resultados da consulta com base em uma ou mais colunas, em ordem ascendente ou descendente.

`JOIN`: Combina registros de duas ou mais tabelas em uma consulta, com base em uma condição de associação entre elas.

`INNER JOIN`: Retorna apenas os registros que têm correspondências em ambas as tabelas.

`LEFT JOIN (ou LEFT OUTER JOIN)`: Retorna todos os registros da tabela à esquerda (primeira tabela mencionada) e os registros correspondentes da tabela à direita (segunda tabela mencionada).

`RIGHT JOIN (ou RIGHT OUTER JOIN)`: Retorna todos os registros da tabela à direita (segunda tabela mencionada) e os registros correspondentes da tabela à esquerda (primeira tabela mencionada).

`FULL JOIN (ou FULL OUTER JOIN)`: Retorna todos os registros quando há uma correspondência em uma das tabelas. Preenche os espaços vazios com NULLs quando não há correspondência.

`UNION`: Combina o resultado de duas ou mais consultas em uma única tabela de resultados.

`INTERSECT`: Retorna todos os registros que são comuns a duas ou mais consultas.

`EXCEPT (ou MINUS)`: Retorna todos os registros da primeira consulta que não estão presentes nas outras consultas.

`DISTINCT`: Retorna apenas valores distintos das colunas selecionadas.

## Banco de Dados Relacional

Um **banco de dados relacional** é um sistema de gerenciamento de banco de dados (SGBD) que organiza e acessa dados com base no modelo relacional. Esse modelo utiliza tabelas para representar e armazenar dados, onde cada tabela é composta por linhas e colunas. Aqui está uma visão geral de como funciona um banco de dados relacional:

* **Tabelas**: Os dados em um banco de dados relacional são organizados em tabelas. Cada tabela é composta por colunas e linhas. As colunas representam os diferentes atributos ou campos dos dados, enquanto as linhas representam as entradas individuais ou registros.

*  **Chaves Primárias**: Cada tabela geralmente tem uma coluna ou conjunto de colunas que atuam como chaves primárias. Uma chave primária é uma coluna ou conjunto de colunas que identifica de forma exclusiva cada registro na tabela.

* **Relacionamentos**: Nos bancos de dados relacionais, os relacionamentos entre tabelas são estabelecidos por meio de chaves estrangeiras. Uma chave estrangeira em uma tabela faz referência à chave primária em outra tabela, estabelecendo uma relação entre os dados nas duas tabelas.

* **Consultas**: Os usuários podem recuperar, atualizar, inserir e excluir dados de um banco de dados relacional por meio de consultas SQL (Structured Query Language). As consultas SQL permitem aos usuários especificar quais dados desejam recuperar ou manipular, bem como definir critérios de filtro, ordenação e agregação.

* **Integridade Referencial**: Um dos princípios fundamentais dos bancos de dados relacionais é a integridade referencial. Isso garante que os relacionamentos entre as tabelas sejam consistentes e precisos, impedindo a inserção de valores inválidos em colunas de chaves estrangeiras.

* **Transações**: Os bancos de dados relacionais suportam transações, que são unidades de trabalho que são executadas de forma consistente e isolada. Isso significa que as operações de inserção, atualização e exclusão podem ser agrupadas em transações, garantindo que as mudanças no banco de dados sejam duráveis e consistentes.

* **Índices**: Para melhorar o desempenho das consultas, os bancos de dados relacionais podem usar índices. Um índice é uma estrutura de dados que permite que o banco de dados localize rapidamente registros com base nos valores de uma ou mais colunas.

> [!IMPORTANT]
> No geral, um banco de dados relacional oferece uma estrutura flexível e poderosa para armazenar e gerenciar dados, permitindo que os usuários representem relações complexas entre os dados e executem consultas sofisticadas para recuperar informações conforme necessário.

## Qual a diferença entre Chave Primária (Primary Key) e Chave Estrangeira (Foreign Key)? 

> [!TIP]
> Pergunta de entrevista! Uma vez me perguntaram justamente essa pergunta em uma entrevista. É um dos assuntos mais importantes de Banco de Dados. Portanto, é importante lembrar e saber explicar bem a diferença entre esses dois conceitos. 

>*Uma chave primária e uma chave estrangeira são conceitos fundamentais em bancos de dados relacionais, como aqueles baseados em SQL (Structured Query Language). Ambas desempenham papéis essenciais na definição da estrutura de um banco de dados e na garantia da integridade dos dados. Aqui está a diferença entre elas:*

* **Chave Primária (Primary Key)**:

Uma chave primária é um campo (ou conjunto de campos) em uma tabela de banco de dados que identifica de forma exclusiva cada registro na tabela.
Uma tabela pode ter apenas uma chave primária.
A chave primária não pode ter valores nulos (NULL) e deve ser única para cada registro.
A chave primária é usada como um identificador exclusivo e é frequentemente usada para indexação, o que melhora o desempenho em operações de consulta.
Por exemplo, em uma tabela de "clientes", o número de identificação do cliente pode ser escolhido como chave primária, garantindo que cada cliente tenha um identificador único.

* **Chave Estrangeira (Foreign Key)**:

Uma chave estrangeira é um campo em uma tabela que está vinculado a chave primária de outra tabela.
A chave estrangeira estabelece uma relação entre duas tabelas, permitindo que os dados relacionados sejam conectados.
Enquanto uma chave primária identifica de forma exclusiva registros em sua própria tabela, uma chave estrangeira permite que registros em uma tabela estejam relacionados a registros em outra tabela.
A chave estrangeira não precisa ser única, e pode haver várias ocorrências do mesmo valor na tabela.
Por exemplo, em uma tabela de "pedidos", pode haver uma chave estrangeira que faz referência à chave primária da tabela "clientes", estabelecendo uma relação entre os clientes que fazem pedidos e os próprios pedidos.


`Em resumo, enquanto a chave primária identifica de forma exclusiva os registros em uma tabela, a chave estrangeira estabelece relações entre registros em diferentes tabelas. Esses conceitos são essenciais para a modelagem de dados em bancos de dados relacionais e para garantir a integridade dos dados.`

