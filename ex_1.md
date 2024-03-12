# Exercise 1


## ex_01

寫出可以得到下方結果的 SQL 語句

Answer

```sql
    SELECT lastname,firstname,jobtitle FROM employees
    WHERE jobtitle = 'Sales Rep';
```

Output

```
+-----------+-----------+-----------+
| lastname  | firstname | jobtitle  |
+-----------+-----------+-----------+
| Jennings  | Leslie    | Sales Rep |
| Thompson  | Leslie    | Sales Rep |
| Firrelli  | Julie     | Sales Rep |
| Patterson | Steve     | Sales Rep |
| Tseng     | Foon Yue  | Sales Rep |
| Vanauf    | George    | Sales Rep |
| Bondur    | Loui      | Sales Rep |
| Hernandez | Gerard    | Sales Rep |
| Castillo  | Pamela    | Sales Rep |
| Bott      | Larry     | Sales Rep |
| Jones     | Barry     | Sales Rep |
| Fixter    | Andy      | Sales Rep |
| Marsh     | Peter     | Sales Rep |
| King      | Tom       | Sales Rep |
| Nishi     | Mami      | Sales Rep |
| Kato      | Yoshimi   | Sales Rep |
| Gerard    | Martin    | Sales Rep |
+-----------+-----------+-----------+
17 rows in set (0.00 sec)
```

## ex_02

寫出可以得到下方結果的 SQL 語句

Answer

```sql
    SELECT lastname,firstname,jobtitle,officeCode FROM employees
    WHERE firstname = 'Leslie'
```

Output

```
+----------+-----------+-----------+------------+
| lastname | firstname | jobtitle  | officeCode |
+----------+-----------+-----------+------------+
| Jennings | Leslie    | Sales Rep | 1          |
| Thompson | Leslie    | Sales Rep | 1          |
+----------+-----------+-----------+------------+
2 rows in set (0.00 sec)
```

## ex_03

寫出可以得到下方結果的 SQL 語句

Answer

```sql
    SELECT firstname,lastname,officeCode FROM employees
    WHERE officeCode <= 3
```

Output

```
+-----------+-----------+------------+
| firstName | lastName  | officeCode |
+-----------+-----------+------------+
| Diane     | Murphy    | 1          |
| Mary      | Patterson | 1          |
| Jeff      | Firrelli  | 1          |
| Anthony   | Bow       | 1          |
| Leslie    | Jennings  | 1          |
| Leslie    | Thompson  | 1          |
| Julie     | Firrelli  | 2          |
| Steve     | Patterson | 2          |
| Foon Yue  | Tseng     | 3          |
| George    | Vanauf    | 3          |
+-----------+-----------+------------+
10 rows in set (0.00 sec)
```


## ex_04

寫出可以得到下方結果的 SQL 語句

Answer

```sql
    SELECT contactLastname,contactFirstname FROM customers
    ORDER BY contactLastname DESC
```

Output

```
+-----------------+------------------+
| contactLastname | contactFirstname |
+-----------------+------------------+
| Young           | Jeff             |
| Young           | Julie            |
| Young           | Mary             |
| Young           | Dorothy          |
| Yoshido         | Juri             |
| Walker          | Brydey           |
| Victorino       | Wendy            |
| Urs             | Braun            |
| Tseng           | Jerry            |
....
```


## ex_05

寫出可以得到下方結果的 SQL 語句

Answer

```sql
    SELECT lastname,firstname,officeCode FROM employees
    where officeCode >= 6
```

Output

```
+-----------+-----------+------------+
| lastname  | firstname | officeCode |
+-----------+-----------+------------+
| Patterson | William   | 6          |
| Bott      | Larry     | 7          |
| Jones     | Barry     | 7          |
| Fixter    | Andy      | 6          |
| Marsh     | Peter     | 6          |
| King      | Tom       | 6          |
+-----------+-----------+------------+
6 rows in set (0.00 sec)
```


## ex_06

寫出可以得到下方結果的 SQL 語句

Answer

```sql
    SELECT lastname,firstname,jobtitle,officeCode FROM employees
    where firstname = 'Leslie'
```

Output

```
+----------+-----------+-----------+------------+
| lastname | firstname | jobtitle  | officeCode |
+----------+-----------+-----------+------------+
| Jennings | Leslie    | Sales Rep | 1          |
| Thompson | Leslie    | Sales Rep | 1          |
+----------+-----------+-----------+------------+
2 rows in set (0.00 sec)
```


## ex_07

寫出可以得到下方結果的 SQL 語句

Answer

```sql
    SELECT lastname FROM employees
    ORDER BY lastname
```

Output

```
+-----------+
| lastname  |
+-----------+
| Bondur    |
| Bott      |
| Bow       |
| Castillo  |
| Firrelli  |

...
| Nishi     |
| Patterson |
| Thompson  |
| Tseng     |
| Vanauf    |
+-----------+
19 rows in set (0.01 sec)
```


## ex_08

寫出可以得到下方結果的 SQL 語句

Answer

```sql
    SELECT customername,country,`state` FROM customers
    WHERE country = 'USA' AND `state` = 'CA'
```

Output

```
+------------------------------+---------+-------+
| customername                 | country | state |
+------------------------------+---------+-------+
| Mini Gifts Distributors Ltd. | USA     | CA    |
| Mini Wheels Co.              | USA     | CA    |
| Technics Stores Inc.         | USA     | CA    |
| Toys4GrownUps.com            | USA     | CA    |
| Boards & Toys Co.            | USA     | CA    |
| Collectable Mini Designs Co. | USA     | CA    |
| Corporate Gift Ideas Co.     | USA     | CA    |
| Men 'R' US Retailers, Ltd.   | USA     | CA    |
| The Sharp Gifts Warehouse    | USA     | CA    |
| West Coast Collectables Co.  | USA     | CA    |
| Signal Collectibles Ltd.     | USA     | CA    |
+------------------------------+---------+-------+
11 rows in set (0.00 sec)
```

## ex_09

寫出可以得到下方結果的 SQL 語句

Answer

```sql
    SELECT customername,country,`state`,creditlimit FROM customers
    WHERE country = 'USA' AND `state` = 'CA' AND creditlimit >= 105000  
```

Output

```
+------------------------------+---------+-------+-------------+
| customername                 | country | state | creditlimit |
+------------------------------+---------+-------+-------------+
| Mini Gifts Distributors Ltd. | USA     | CA    |   210500.00 |
| Collectable Mini Designs Co. | USA     | CA    |   105000.00 |
| Corporate Gift Ideas Co.     | USA     | CA    |   105000.00 |
+------------------------------+---------+-------+-------------+
3 rows in set (0.00 sec)
```

## ex_10

寫出可以得到下方結果的 SQL 語句

Answer

```sql
    SELECT officeCode,city,phone,country FROM offices
    LIMIT 4
```

Output

```
+------------+---------------+-----------------+---------+
| officeCode | city          | phone           | country |
+------------+---------------+-----------------+---------+
| 1          | San Francisco | +1 650 219 4782 | USA     |
| 2          | Boston        | +1 215 837 0825 | USA     |
| 3          | NYC           | +1 212 555 3000 | USA     |
| 4          | Paris         | +33 14 723 4404 | France  |
+------------+---------------+-----------------+---------+
4 rows in set (0.01 sec)
```