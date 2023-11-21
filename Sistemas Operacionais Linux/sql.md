-- SELECT: Recupera dados de uma ou mais tabelas.

`SELECT column1, column2 FROM table WHERE condition;`

-- FROM: Especifica a tabela da qual os dados são recuperados.

`SELECT column1, column2 FROM table;`

-- WHERE: Filtra os resultados com base em uma condição.

`SELECT column1, column2 FROM table WHERE condition;`

-- ORDER BY: Classifica os resultados por uma ou mais colunas.

`SELECT column1, column2 FROM table ORDER BY column1 ASC;`

-- GROUP BY: Agrupa os resultados com base em uma ou mais colunas.

`SELECT column1, COUNT(*) FROM table GROUP BY column1;`

-- HAVING: Filtra os resultados de uma cláusula GROUP BY com base em uma condição.

`SELECT column1, COUNT(*) FROM table GROUP BY column1 HAVING COUNT(*) > 1;`

-- JOIN: Combina linhas de duas ou mais tabelas com base em uma condição relacionada.

`SELECT column1, column2 FROM table1 INNER JOIN table2 ON table1.id = table2.id;`

-- LEFT JOIN (ou LEFT OUTER JOIN): Retorna todos os registros da tabela à esquerda e os registros correspondentes da tabela à direita. Se não houver correspondência, os resultados da tabela à direita conterão valores nulos.

`SELECT column1, column2 FROM table1 LEFT JOIN table2 ON table1.id = table2.id;`

-- RIGHT JOIN (ou RIGHT OUTER JOIN): Retorna todos os registros da tabela à direita e os registros correspondentes da tabela à esquerda. Se não houver correspondência, os resultados da tabela à esquerda conterão valores nulos.

`SELECT column1, column2 FROM table1 RIGHT JOIN table2 ON table1.id = table2.id;
`
-- FULL JOIN (ou FULL OUTER JOIN): Retorna todos os registros quando há uma correspondência em uma das tabelas. Os registros não correspondentes nas tabelas à esquerda e à direita conterão valores nulos.

`SELECT column1, column2 FROM table1 FULL JOIN table2 ON table1.id = table2.id;`

-- CROSS JOIN: Retorna o produto cartesiano de ambas as tabelas, ou seja, combina cada linha da tabela à esquerda com cada linha da tabela à direita.

`SELECT column1, column2 FROM table1 CROSS JOIN table2;`

-- DISTINCT: Retorna valores distintos de uma coluna.

`SELECT DISTINCT column1 FROM table;
`
-- INSERT INTO: Insere novas linhas em uma tabela.

`INSERT INTO table (column1, column2) VALUES (value1, value2);
`
-- UPDATE: Atualiza dados existentes em uma tabela.

`UPDATE table SET column1 = value1 WHERE condition;
`
-- DELETE FROM: Exclui linhas de uma tabela.

`DELETE FROM table WHERE condition;
`
