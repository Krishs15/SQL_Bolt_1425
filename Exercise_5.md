#Exercise_5

#1.List all the Canadian cities and their populations 

#Query
```sql
SELECT city,population FROM north_american_cities
WHERE country='Canada';
```

#Output
| city | population |
|---|---|
| Toronto | 2795060 |
| Montreal | 1717767 |

#2.Order all the cities in the United States by their latitude from north to south

#Query
```sql
SELECT city FROM north_american_cities
WHERE country='United States' 
ORDER BY latitude DESC;
```

#Output
| city |
|---|
| Chicago |
| New York |
| Philadelphia |
| Los Angeles |
| Phoenix |
| Houston |

#3.List all the cities west of Chicago, ordered from west to east

#Query
```sql
SELECT * FROM north_american_cities 
WHERE longitude < (SELECT longitude FROM north_american_cities WHERE city = 'Chicago') 
ORDER BY longitude ASC;
```

#Output
| city | country | population | latitude | longitude |
|---|---|---|---|---|
| Los Angeles | United States | 3884307 | 34.052234 | -118.243685 |
| Phoenix | United States | 1513367 | 33.448377 | -112.074037 |
| Guadalajara | Mexico | 1500800 | 20.659699 | -103.349609 |
| Mexico City | Mexico | 8555500 | 19.432608 | -99.133208 |
| Ecatepec de Morelos | Mexico | 1742000 | 19.601841 | -99.050674 |
| Houston | United States | 2195914 | 29.760427 | -95.369803 |

#4.List the two largest cities in Mexico (by population)

#Query
```sql
SELECT city 
FROM north_american_cities 
WHERE country = 'Mexico' 
ORDER BY population DESC 
LIMIT 2;
```

#Output
| city |
|---|
| Mexico City |
| Ecatepec de Morelos |

#5.List the third and fourth largest cities (by population) in the United States and their population

#Query
```sql
SELECT city, population 
FROM north_american_cities 
WHERE country = 'United States' 
ORDER BY population DESC 
LIMIT 2 OFFSET 2;
```

#Output
| city | population |
|---|---|
| Chicago | 2718782 |
| Houston | 2195914 |