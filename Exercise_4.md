#Exercise_4

#1.List all directors of Pixar movies (alphabetically), without duplicates 

#Query
```sql
 SELECT DISTINCT director FROM movies
ORDER BY director ASC;
```

#Output
| director |
|---|
| Andrew Stanton |
| Brad Bird |
| Brenda Chapman |
| Dan Scanlon |
| John Lasseter |
| Lee Unkrich |
| Pete Docter |

#2.List the last four Pixar movies released (ordered from most recent to least)

#Query
```sql
SELECT * FROM movies 
ORDER BY year DESC
LIMIT 4;
```

#Output
| id | title | director | year | length_minutes |
|---|---|---|---|---|
| 1 | Monsters University | Dan Scanlon | 2013 | 110 |
| 8 | Brave | Brenda Chapman | 2012 | 102 |
| 9 | Cars 2 | John Lasseter | 2011 | 120 |
| 13 | Toy Story 3 | Lee Unkrich | 2010 | 103 |

#3.List the first five Pixar movies sorted alphabetically

#Query
```sql
SELECT * FROM movies 
ORDER BY title ASC 
LIMIT 5;
```

#Output
| id | title | director | year | length_minutes |
|---|---|---|---|---|
| 6 | A Bug's Life | John Lasseter | 1998 | 95 |
| 8 | Brave | Brenda Chapman | 2012 | 102 |
| 7 | Cars | John Lasseter | 2006 | 117 |
| 9 | Cars 2 | John Lasseter | 2011 | 120 |
| 12 | Finding Nemo | Andrew Stanton | 2003 | 107 |

#4.List the next five Pixar movies sorted alphabetically

#Query
```sql
SELECT * FROM movies 
ORDER BY title ASC 
LIMIT 5 OFFSET 5;
```

#Output
| id | title | director | year | length_minutes |
|---|---|---|---|---|
| 1 | Monsters University | Dan Scanlon | 2013 | 110 |
| 4 | Monsters, Inc. | Pete Docter | 2001 | 92 |
| 11 | Ratatouille | Brad Bird | 2007 | 115 |
| 10 | The Incredibles | Brad Bird | 2004 | 116 |
| 2 | Toy Story | John Lasseter | 1995 | 81 |