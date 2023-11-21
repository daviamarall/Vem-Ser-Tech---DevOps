**-- SELECT: Recupera dados de uma ou mais tabelas.**

`SELECT column1, column2 FROM table WHERE condition;`

**-- FROM: Especifica a tabela da qual os dados são recuperados.**

`SELECT column1, column2 FROM table;`

**-- WHERE: Filtra os resultados com base em uma condição.**

`SELECT column1, column2 FROM table WHERE condition;`

**-- ORDER BY: Classifica os resultados por uma ou mais colunas.**

`SELECT column1, column2 FROM table ORDER BY column1 ASC;`

**-- GROUP BY: Agrupa os resultados com base em uma ou mais colunas.**

`SELECT column1, COUNT(*) FROM table GROUP BY column1;`

**-- HAVING: Filtra os resultados de uma cláusula GROUP BY com base em uma condição.**

`SELECT column1, COUNT(*) FROM table GROUP BY column1 HAVING COUNT(*) > 1;`

**-- JOIN: Combina linhas de duas ou mais tabelas com base em uma condição relacionada.**

`SELECT column1, column2 FROM table1 INNER JOIN table2 ON table1.id = table2.id;`

**-- LEFT JOIN (ou LEFT OUTER JOIN): Retorna todos os registros da tabela à esquerda e os registros correspondentes da tabela à direita. Se não houver correspondência, os resultados da tabela à direita conterão valores nulos.**

`SELECT column1, column2 FROM table1 LEFT JOIN table2 ON table1.id = table2.id;`

**-- RIGHT JOIN (ou RIGHT OUTER JOIN): Retorna todos os registros da tabela à direita e os registros correspondentes da tabela à esquerda. Se não houver correspondência, os resultados da tabela à esquerda conterão valores nulos.**

`SELECT column1, column2 FROM table1 RIGHT JOIN table2 ON table1.id = table2.id;
`

**-- FULL JOIN (ou FULL OUTER JOIN): Retorna todos os registros quando há uma correspondência em uma das tabelas. Os registros não correspondentes nas tabelas à esquerda e à direita conterão valores nulos.**

`SELECT column1, column2 FROM table1 FULL JOIN table2 ON table1.id = table2.id;`

**-- CROSS JOIN: Retorna o produto cartesiano de ambas as tabelas, ou seja, combina cada linha da tabela à esquerda com cada linha da tabela à direita.**

`SELECT column1, column2 FROM table1 CROSS JOIN table2;`

**-- DISTINCT: Retorna valores distintos de uma coluna.**

`SELECT DISTINCT column1 FROM table;
`

**-- Exemplo com MAX: Retorna o valor máximo da coluna2 da tabela.**

`SELECT MAX(column2) AS max_value FROM table;`

**-- Exemplo com MIN: Retorna o valor mínimo da coluna2 da tabela.**

`SELECT MIN(column2) AS min_value FROM table;`

**-- Exemplo com AVG: Retorna a média da coluna2 da tabela.**

`SELECT AVG(column2) AS average_value FROM table;`

**-- Exemplo com SUM: Retorna a soma da coluna2 da tabela.**

`SELECT SUM(column2) AS sum_value FROM table;`

**-- Exemplo com COUNT: Retorna o número de registros na tabela.**

`SELECT COUNT(*) AS record_count FROM table;`

**-- Exemplo com JOIN e Igual: Combina linhas de duas tabelas onde a coluna1 é igual.**

SELECT table1.column1, table1.column2, table2.column2
FROM table1
JOIN table2 ON table1.column1 = table2.column1;




**-- INSERT INTO: Insere novas linhas em uma tabela.**

`INSERT INTO table (column1, column2) VALUES (value1, value2);
`

**-- UPDATE: Atualiza dados existentes em uma tabela.**

`UPDATE table SET column1 = value1 WHERE condition;
`

**-- DELETE FROM: Exclui linhas de uma tabela.**

`DELETE FROM table WHERE condition;
`

### Condições 

**-- Igual: Retorna registros onde o valor da coluna1 é igual a 'valor'.**

SELECT column1, column2 FROM table WHERE column1 = 'valor';

**-- Diferente: Retorna registros onde o valor da coluna1 é diferente de 'valor'.**

SELECT column1, column2 FROM table WHERE column1 <> 'valor';

**-- Maior que: Retorna registros onde o valor da coluna1 é maior que 5.**

SELECT column1, column2 FROM table WHERE column1 > 5;

**-- Menor que: Retorna registros onde o valor da coluna1 é menor que 10.**

SELECT column1, column2 FROM table WHERE column1 < 10;

**-- Maior ou igual: Retorna registros onde o valor da coluna1 é maior ou igual a 10.**

SELECT column1, column2 FROM table WHERE column1 >= 10;

**-- Menor ou igual: Retorna registros onde o valor da coluna1 é menor ou igual a 20.**

SELECT column1, column2 FROM table WHERE column1 <= 20;

**-- IN: Retorna registros onde o valor da coluna1 está em um conjunto específico.**

SELECT column1, column2 FROM table WHERE column1 IN ('valor1', 'valor2', 'valor3');

**-- NOT IN: Retorna registros onde o valor da coluna1 não está em um conjunto específico.**

SELECT column1, column2 FROM table WHERE column1 NOT IN ('valor1', 'valor2', 'valor3');

**-- LIKE: Retorna registros onde o valor da coluna1 corresponde a um padrão ('prefixo%').**

SELECT column1, column2 FROM table WHERE column1 LIKE 'prefixo%';

**-- BETWEEN: Retorna registros onde o valor da coluna1 está entre 10 e 20.**

SELECT column1, column2 FROM table WHERE column1 BETWEEN 10 AND 20;

**-- IS NULL: Retorna registros onde o valor da coluna1 é nulo.**

SELECT column1, column2 FROM table WHERE column1 IS NULL;

**-- IS NOT NULL: Retorna registros onde o valor da coluna1 não é nulo.**

SELECT column1, column2 FROM table WHERE column1 IS NOT NULL;
