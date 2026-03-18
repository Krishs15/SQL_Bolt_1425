# Exercise_2

## 1.Find the movie with a row id of 6

## Query
```sql
     SELECT title FROM movies WHERE id=6;
```

## Output
|title|
|---|
|The Incredibles|

## 2.Find the movies released in the years between 2000 and 2010

## Query
```sql
     SELECT * FROM movies WHERE year BETWEEN 2000 AND 2010;
```

## Output
| id | title | director | year | length_minutes |
|---|---|---|---|---|
| 4 | Monsters, Inc. | Pete Docter | 2001 | 92 |
| 5 | Finding Nemo | Andrew Stanton | 2003 | 107 |
| 6 | The Incredibles | Brad Bird | 2004 | 116 |
| 7 | Cars | John Lasseter | 2006 | 117 |
| 8 | Ratatouille | Brad Bird | 2007 | 115 |
| 9 | WALL-E | Andrew Stanton | 2008 | 104 |
| 10 | Up | Pete Docter | 2009 | 101 |
| 11 | Toy Story 3 | Lee Unkrich | 2010 | 103 |

## 3.Find the movies not released in the years between 2000 and 2010 

## Query
```sql
     SELECT * FROM movies WHERE year NOT BETWEEN 2000 AND 2010;
```

## Output
| id | title | director | year | length_minutes |
|---|---|---|---|---|
| 1 | Toy Story | John Lasseter | 1995 | 81 |
| 2 | A Bug's Life | John Lasseter | 1998 | 95 |
| 3 | Toy Story 2 | John Lasseter | 1999 | 93 |
| 12 | Cars 2 | John Lasseter | 2011 | 120 |
| 13 | Brave | Brenda Chapman | 2012 | 102 |
| 14 | Monsters University | Dan Scanlon | 2013 | 110 |

## 4.Find the first 5 Pixar movies and their release year

## Query
```sql
     SELECT title,year FROM movies ORDER BY year ASC LIMIT 5;
```

## Output
| title | year |
|---|---|
| Toy Story | 1995 |
| A Bug's Life | 1998 |
| Toy Story 2 | 1999 |
| Monsters, Inc. | 2001 |
| Finding Nemo | 2003 |
