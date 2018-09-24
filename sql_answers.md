Questions
Return ALL the data in the 'movies' table.

```SELECT * FROM movies


1	Iron Man	2008	15:35
2	The Incredible Hulk	2008	22:05
3	Iron Man 2	2010	18:00
4	Thor	2011	21:20
5	Captain America: The First Avenger	2011	13:10
6	Avengers Assemble	2012	14:30
7	Iron Man 3	2013	21:55
8	Thor: The Dark World	2013	15:20
9	Batman Begins	2005	20:30
10	Captain America: The Winter Soldier	2014	21:10
11	Guardians of the Galaxy	2014	16:20
12	Avengers: Age of Ultron	2015	23:00
13	Ant-Man	2015	13:25
14	Captain America: Civil War	2016	14:45
15	Doctor Strange	2016	22:40
16	Guardians of the Galaxy 2	2017	22:00
17	Spider-Man: Homecoming	2017	18:10
18	Thor: Ragnarok	2017	19:35
19	Black Panther	2018	22:20
```

Return ONLY the name column from the 'people' table

```SELECT name FROM people

Ana Martinez
Andrew Carracher
Caroline Graves
Genna-Lee Walsh
Graham Stein
Iain Floyd
Iona Wright
Jackie Farr
Jennifer Proctor
Jordan Raitt
Katherine Jeffree
Kris McElhinney
Michael Griffin
Monica Mateiu
Nathan Atkinson
Nyalls Hemingway
Oksana Richards
Rana Akbar
Tavy Fraser
Thomas Gracie
Xavier Godard
Kith Douglas```


Oops! Someone at CodeClan spelled Keith's name wrong! Change it to reflect the proper spelling.

```UPDATE people
SET name = 'Keith Douglas'
WHERE name = 'Kith Douglas';

1	Ana Martinez
2	Andrew Carracher
3	Caroline Graves
4	Genna-Lee Walsh
5	Graham Stein
6	Iain Floyd
7	Iona Wright
8	Jackie Farr
9	Jennifer Proctor
10	Jordan Raitt
11	Katherine Jeffree
12	Kris McElhinney
13	Michael Griffin
14	Monica Mateiu
15	Nathan Atkinson
16	Nyalls Hemingway
17	Oksana Richards
18	Rana Akbar
19	Tavy Fraser
20	Thomas Gracie
21	Xavier Godard
22	Keith Douglas```

Return ONLY your name from the 'people' table.

SELECT * from people
WHERE name = 'Kris McElhinney'

12	Kris McElhinney

The cinema is showing 'Batman Begins', but Batman is DC, not Marvel! Delete the entry from the 'movies' table.

DELETE from movies
WHERE title = 'Batman Begins'

1	Iron Man	2008	15:35
2	The Incredible Hulk	2008	22:05
3	Iron Man 2	2010	18:00
4	Thor	2011	21:20
5	Captain America: The First Avenger	2011	13:10
6	Avengers Assemble	2012	14:30
7	Iron Man 3	2013	21:55
8	Thor: The Dark World	2013	15:20
10	Captain America: The Winter Soldier	2014	21:10
11	Guardians of the Galaxy	2014	16:20
12	Avengers: Age of Ultron	2015	23:00
13	Ant-Man	2015	13:25
14	Captain America: Civil War	2016	14:45
15	Doctor Strange	2016	22:40
16	Guardians of the Galaxy 2	2017	22:00
17	Spider-Man: Homecoming	2017	18:10
18	Thor: Ragnarok	2017	19:35
19	Black Panther	2018	22:20

Create a new entry in the 'people' table with the name of one of the instructors.

INSERT INTO people (id, name)
VALUES (23, 'Craig Morton');

1	Ana Martinez
2	Andrew Carracher
3	Caroline Graves
4	Genna-Lee Walsh
5	Graham Stein
6	Iain Floyd
7	Iona Wright
8	Jackie Farr
9	Jennifer Proctor
10	Jordan Raitt
11	Katherine Jeffree
12	Kris McElhinney
13	Michael Griffin
14	Monica Mateiu
15	Nathan Atkinson
16	Nyalls Hemingway
17	Oksana Richards
18	Rana Akbar
19	Tavy Fraser
20	Thomas Gracie
21	Xavier Godard
22	Kith Douglas
23	Craig Morton

Pawel has decided to hijack our movie evening, Remove him from the table of people.

INSERT INTO people (id, name)
VALUES (24, 'Pawel Orzechowski');

1	Ana Martinez
2	Andrew Carracher
3	Caroline Graves
4	Genna-Lee Walsh
5	Graham Stein
6	Iain Floyd
7	Iona Wright
8	Jackie Farr
9	Jennifer Proctor
10	Jordan Raitt
11	Katherine Jeffree
12	Kris McElhinney
13	Michael Griffin
14	Monica Mateiu
15	Nathan Atkinson
16	Nyalls Hemingway
17	Oksana Richards
18	Rana Akbar
19	Tavy Fraser
20	Thomas Gracie
21	Xavier Godard
22	Kith Douglas
23	Craig Morton
24	Pawel Orzechowski

DELETE from people
WHERE id = 24;

1	Ana Martinez
2	Andrew Carracher
3	Caroline Graves
4	Genna-Lee Walsh
5	Graham Stein
6	Iain Floyd
7	Iona Wright
8	Jackie Farr
9	Jennifer Proctor
10	Jordan Raitt
11	Katherine Jeffree
12	Kris McElhinney
13	Michael Griffin
14	Monica Mateiu
15	Nathan Atkinson
16	Nyalls Hemingway
17	Oksana Richards
18	Rana Akbar
19	Tavy Fraser
20	Thomas Gracie
21	Xavier Godard
22	Kith Douglas
23	Craig Morton


The cinema has just heard that they will be holding an exclusive midnight showing of 'Avengers: Infinity War'!! Create a new entry in the 'movies' table to reflect this.

INSERT into movies (id, title, year, show_time)
VALUES (20, 'Avengers: Infinity War', 2018, '23:59');

1	Iron Man	2008	15:35
2	The Incredible Hulk	2008	22:05
3	Iron Man 2	2010	18:00
4	Thor	2011	21:20
5	Captain America: The First Avenger	2011	13:10
6	Avengers Assemble	2012	14:30
7	Iron Man 3	2013	21:55
8	Thor: The Dark World	2013	15:20
10	Captain America: The Winter Soldier	2014	21:10
11	Guardians of the Galaxy	2014	16:20
12	Avengers: Age of Ultron	2015	23:00
13	Ant-Man	2015	13:25
14	Captain America: Civil War	2016	14:45
15	Doctor Strange	2016	22:40
16	Guardians of the Galaxy 2	2017	22:00
17	Spider-Man: Homecoming	2017	18:10
18	Thor: Ragnarok	2017	19:35
19	Black Panther	2018	22:20
20	Avengers: Infinity War	2018	23:59

The cinema would also like to make the Guardians movies a back to back feature. Find out the show time of "Guardians of the Galaxy" and set the show time of "Guardians of the Galaxy 2" to start two hours later.

UPDATE movies
SET show_time = '24:00'
WHERE id = 16;

1	Iron Man	2008	15:35
2	The Incredible Hulk	2008	22:05
3	Iron Man 2	2010	18:00
4	Thor	2011	21:20
5	Captain America: The First Avenger	2011	13:10
6	Avengers Assemble	2012	14:30
7	Iron Man 3	2013	21:55
8	Thor: The Dark World	2013	15:20
10	Captain America: The Winter Soldier	2014	21:10
11	Guardians of the Galaxy	2014	16:20
12	Avengers: Age of Ultron	2015	23:00
13	Ant-Man	2015	13:25
14	Captain America: Civil War	2016	14:45
15	Doctor Strange	2016	22:40
16	Guardians of the Galaxy 2	2017	24:00
17	Spider-Man: Homecoming	2017	18:10
18	Thor: Ragnarok	2017	19:35
19	Black Panther	2018	22:20
20	Avengers: Infinity War	2018	23:59

Extension

Delete multiple entries from your table in a single command.

DELETE FROM movies;

:)

or when I reloaded my marvel dataset

DELETE FROM movies
WHERE title LIKE '%Guardians%';

1	Iron Man	2008	15:35
2	The Incredible Hulk	2008	22:05
3	Iron Man 2	2010	18:00
4	Thor	2011	21:20
5	Captain America: The First Avenger	2011	13:10
6	Avengers Assemble	2012	14:30
7	Iron Man 3	2013	21:55
8	Thor: The Dark World	2013	15:20
9	Batman Begins	2005	20:30
10	Captain America: The Winter Soldier	2014	21:10
11	Guardians of the Galaxy	2014	16:20
12	Avengers: Age of Ultron	2015	23:00
13	Ant-Man	2015	13:25
14	Captain America: Civil War	2016	14:45
15	Doctor Strange	2016	22:40
16	Guardians of the Galaxy 2	2017	22:00
17	Spider-Man: Homecoming	2017	18:10
18	Thor: Ragnarok	2017	19:35
19	Black Panther	2018	22:20

Select all the movies ordered by year in descending order

SELECT * from movies
ORDER BY title DESC


8	Thor: The Dark World	2013	15:20
18	Thor: Ragnarok	2017	19:35
4	Thor	2011	21:20
2	The Incredible Hulk	2008	22:05
17	Spider-Man: Homecoming	2017	18:10
7	Iron Man 3	2013	21:55
3	Iron Man 2	2010	18:00
1	Iron Man	2008	15:35
15	Doctor Strange	2016	22:40
10	Captain America: The Winter Soldier	2014	21:10
5	Captain America: The First Avenger	2011	13:10
14	Captain America: Civil War	2016	14:45
19	Black Panther	2018	22:20
9	Batman Begins	2005	20:30
12	Avengers: Age of Ultron	2015	23:00
6	Avengers Assemble	2012	14:30
13	Ant-Man	2015	13:25
