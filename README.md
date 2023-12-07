# sql_imdb_movies

### TABLES
```sql
create table genres
(
    id   serial8 primary key,
    name varchar(50) not null
);

create table movies
(
    id           serial8 primary key,
    title        varchar(100) not null,
    release_year int2         not null,
    rating       float4       not null,
    duration     int4         not null
);

create table movies_genres
(
    genre_id int8 not null,
    movie_id int8 not null,
    primary key (genre_id, movie_id),
    foreign key (genre_id) references genres (id) on delete cascade,
    foreign key (movie_id) references movies (id) on delete cascade
);
```

### INSERTS
```sql

insert into genres (name) values ('Drama');
insert into genres (name) values ('Crime');
insert into genres (name) values ('Action');
insert into genres (name) values ('Biography');
insert into genres (name) values ('History');
insert into genres (name) values ('Adventure');
insert into genres (name) values ('Sci-Fi');
insert into genres (name) values ('Romance');
insert into genres (name) values ('Western');
insert into genres (name) values ('Animation');
insert into genres (name) values ('Fantasy');
insert into genres (name) values ('Thriller');
insert into genres (name) values ('Mystery');
insert into genres (name) values ('Family');
insert into genres (name) values ('War');
insert into genres (name) values ('Comedy');
insert into genres (name) values ('Music');
insert into genres (name) values ('Horror');
insert into genres (name) values ('Film-Noir');
insert into genres (name) values ('Musical');



insert into movies (title, release_year, rating, duration) values ('The Shawshank Redemption', 1994, 9.3, 142);
insert into movies (title, release_year, rating, duration) values ('The Godfather', 1972, 9.2, 175);
insert into movies (title, release_year, rating, duration) values ('The Dark Knight', 2008, 9.0, 152);
insert into movies (title, release_year, rating, duration) values ('Schindler s List', 1993, 9.0, 195);
insert into movies (title, release_year, rating, duration) values ('The Lord of the Rings: The Return of the King', 2003, 9.0, 201);
insert into movies (title, release_year, rating, duration) values ('The Godfather Part II', 1974, 9.0, 202);
insert into movies (title, release_year, rating, duration) values ('12 Angry Men', 1957, 9.0, 96);
insert into movies (title, release_year, rating, duration) values ('Pulp Fiction', 1994, 8.9, 154);
insert into movies (title, release_year, rating, duration) values ('Fight Club', 1999, 8.8, 139);
insert into movies (title, release_year, rating, duration) values ('The Lord of the Rings: The Fellowship of the Ring', 2001, 8.8, 178);
insert into movies (title, release_year, rating, duration) values ('Inception', 2010, 8.8, 148);
insert into movies (title, release_year, rating, duration) values ('Forrest Gump', 1994, 8.8, 142);
insert into movies (title, release_year, rating, duration) values ('The Lord of the Rings: The Two Towers', 2002, 8.8, 179);
insert into movies (title, release_year, rating, duration) values ('The Good, the Bad and the Ugly', 1966, 8.8, 178);
insert into movies (title, release_year, rating, duration) values ('Spider-Man: Across the Spider-Verse', 2023, 8.7, 140);
insert into movies (title, release_year, rating, duration) values ('Interstellar', 2014, 8.7, 169);
insert into movies (title, release_year, rating, duration) values ('Goodfellas', 1990, 8.7, 145);
insert into movies (title, release_year, rating, duration) values ('The Matrix', 1999, 8.7, 136);
insert into movies (title, release_year, rating, duration) values ('One Flew Over the Cuckoo s Nest', 1975, 8.7, 133);
insert into movies (title, release_year, rating, duration) values ('Star Wars: Episode V - The Empire Strikes Back', 1980, 8.7, 124);
insert into movies (title, release_year, rating, duration) values ('The Silence of the Lambs', 1991, 8.6, 118);
insert into movies (title, release_year, rating, duration) values ('Se7en', 1995, 8.6, 127);
insert into movies (title, release_year, rating, duration) values ('Spirited Away', 2001, 8.6, 125);
insert into movies (title, release_year, rating, duration) values ('Saving Private Ryan', 1998, 8.6, 169);
insert into movies (title, release_year, rating, duration) values ('The Green Mile', 1999, 8.6, 189);
insert into movies (title, release_year, rating, duration) values ('Star Wars: Episode IV - A New Hope', 1977, 8.6, 121);
insert into movies (title, release_year, rating, duration) values ('City of God', 2002, 8.6, 130);
insert into movies (title, release_year, rating, duration) values ('Terminator 2: Judgment Day', 1991, 8.6, 137);
insert into movies (title, release_year, rating, duration) values ('Life Is Beautiful', 1997, 8.6, 116);
insert into movies (title, release_year, rating, duration) values ('It s a Wonderful Life', 1946, 8.6, 130);
insert into movies (title, release_year, rating, duration) values ('Seven Samurai', 1954, 8.6, 207);
insert into movies (title, release_year, rating, duration) values ('Harakiri', 1962, 8.6, 133);
insert into movies (title, release_year, rating, duration) values ('Oppenheimer', 2023, 8.5, 180);
insert into movies (title, release_year, rating, duration) values ('Whiplash', 2014, 8.5, 106);
insert into movies (title, release_year, rating, duration) values ('Alien', 1979, 8.5, 117);
insert into movies (title, release_year, rating, duration) values ('Gladiator', 2000, 8.5, 155);
insert into movies (title, release_year, rating, duration) values ('Psycho', 1960, 8.5, 109);
insert into movies (title, release_year, rating, duration) values ('Back to the Future', 1985, 8.5, 116);
insert into movies (title, release_year, rating, duration) values ('The Departed', 2006, 8.5, 151);
insert into movies (title, release_year, rating, duration) values ('Parasite', 2019, 8.5, 132);
insert into movies (title, release_year, rating, duration) values ('The Prestige', 2006, 8.5, 130);
insert into movies (title, release_year, rating, duration) values ('Léon: The Professional', 1994, 8.5, 110);
insert into movies (title, release_year, rating, duration) values ('Django Unchained', 2012, 8.5, 165);
insert into movies (title, release_year, rating, duration) values ('American History X', 1998, 8.5, 119);
insert into movies (title, release_year, rating, duration) values ('The Lion King', 1994, 8.5, 88);
insert into movies (title, release_year, rating, duration) values ('The Usual Suspects', 1995, 8.5, 106);
insert into movies (title, release_year, rating, duration) values ('The Pianist', 2002, 8.5, 150);
insert into movies (title, release_year, rating, duration) values ('The Intouchables', 2011, 8.5, 112);
insert into movies (title, release_year, rating, duration) values ('Casablanca', 1942, 8.5, 102);
insert into movies (title, release_year, rating, duration) values ('Rear Window', 1954, 8.5, 112);
insert into movies (title, release_year, rating, duration) values ('Once Upon a Time in the West', 1968, 8.5, 166);
insert into movies (title, release_year, rating, duration) values ('Grave of the Fireflies', 1988, 8.5, 89);
insert into movies (title, release_year, rating, duration) values ('Cinema Paradiso', 1988, 8.5, 155);
insert into movies (title, release_year, rating, duration) values ('Modern Times', 1936, 8.5, 87);
insert into movies (title, release_year, rating, duration) values ('City Lights', 1931, 8.5, 87);
insert into movies (title, release_year, rating, duration) values ('The Shining', 1980, 8.4, 146);
insert into movies (title, release_year, rating, duration) values ('Coco', 2017, 8.4, 105);
insert into movies (title, release_year, rating, duration) values ('Joker', 2019, 8.4, 122);
insert into movies (title, release_year, rating, duration) values ('Spider-Man: Into the Spider-Verse', 2018, 8.4, 117);
insert into movies (title, release_year, rating, duration) values ('Inglourious Basterds', 2009, 8.4, 153);
insert into movies (title, release_year, rating, duration) values ('Avengers: Endgame', 2019, 8.4, 181);
insert into movies (title, release_year, rating, duration) values ('Aliens', 1986, 8.4, 137);
insert into movies (title, release_year, rating, duration) values ('Apocalypse Now', 1979, 8.4, 147);
insert into movies (title, release_year, rating, duration) values ('The Dark Knight Rises', 2012, 8.4, 164);
insert into movies (title, release_year, rating, duration) values ('Oldboy', 2003, 8.4, 120);
insert into movies (title, release_year, rating, duration) values ('Memento', 2000, 8.4, 113);
insert into movies (title, release_year, rating, duration) values ('Come and See', 1985, 8.4, 142);
insert into movies (title, release_year, rating, duration) values ('Avengers: Infinity War', 2018, 8.4, 149);
insert into movies (title, release_year, rating, duration) values ('Raiders of the Lost Ark', 1981, 8.4, 115);
insert into movies (title, release_year, rating, duration) values ('Your Name.', 2016, 8.4, 106);
insert into movies (title, release_year, rating, duration) values ('Amadeus', 1984, 8.4, 160);
insert into movies (title, release_year, rating, duration) values ('3 Idiots', 2009, 8.4, 170);
insert into movies (title, release_year, rating, duration) values ('WALL·E', 2008, 8.4, 98);
insert into movies (title, release_year, rating, duration) values ('The Lives of Others', 2006, 8.4, 137);
insert into movies (title, release_year, rating, duration) values ('Capernaum', 2018, 8.4, 126);
insert into movies (title, release_year, rating, duration) values ('Dr. Strangelove or: How I Learned to Stop Worrying and Love the Bomb', 1964, 8.4, 95);
insert into movies (title, release_year, rating, duration) values ('Das Boot', 1981, 8.4, 149);
insert into movies (title, release_year, rating, duration) values ('Sunset Blvd.', 1950, 8.4, 110);
insert into movies (title, release_year, rating, duration) values ('Witness for the Prosecution', 1957, 8.4, 116);
insert into movies (title, release_year, rating, duration) values ('Paths of Glory', 1957, 8.4, 88);
insert into movies (title, release_year, rating, duration) values ('The Great Dictator', 1940, 8.4, 125);
insert into movies (title, release_year, rating, duration) values ('High and Low', 1963, 8.4, 143);
insert into movies (title, release_year, rating, duration) values ('American Beauty', 1999, 8.3, 122);
insert into movies (title, release_year, rating, duration) values ('Requiem for a Dream', 2000, 8.3, 102);
insert into movies (title, release_year, rating, duration) values ('Good Will Hunting', 1997, 8.3, 126);
insert into movies (title, release_year, rating, duration) values ('Eternal Sunshine of the Spotless Mind', 2004, 8.3, 108);
insert into movies (title, release_year, rating, duration) values ('2001: A Space Odyssey', 1968, 8.3, 149);
insert into movies (title, release_year, rating, duration) values ('Braveheart', 1995, 8.3, 178);
insert into movies (title, release_year, rating, duration) values ('The Hunt', 2012, 8.3, 115);
insert into movies (title, release_year, rating, duration) values ('Once Upon a Time in America', 1984, 8.3, 229);
insert into movies (title, release_year, rating, duration) values ('Reservoir Dogs', 1992, 8.3, 99);
insert into movies (title, release_year, rating, duration) values ('Toy Story', 1995, 8.3, 81);
insert into movies (title, release_year, rating, duration) values ('Lawrence of Arabia', 1962, 8.3, 218);
insert into movies (title, release_year, rating, duration) values ('Star Wars: Episode VI - Return of the Jedi', 1983, 8.3, 131);
insert into movies (title, release_year, rating, duration) values ('Princess Mononoke', 1997, 8.3, 134);
insert into movies (title, release_year, rating, duration) values ('Singin  in the Rain', 1952, 8.3, 103);
insert into movies (title, release_year, rating, duration) values ('Toy Story 3', 2010, 8.3, 103);
insert into movies (title, release_year, rating, duration) values ('Citizen Kane', 1941, 8.3, 119);
insert into movies (title, release_year, rating, duration) values ('The Apartment', 1960, 8.3, 125);
insert into movies (title, release_year, rating, duration) values ('Ikiru', 1952, 8.3, 143);


insert into movies_genres (movie_id, genre_id) values (1, 1);
insert into movies_genres (movie_id, genre_id) values (2, 2);
insert into movies_genres (movie_id, genre_id) values (2, 1);
insert into movies_genres (movie_id, genre_id) values (3, 3);
insert into movies_genres (movie_id, genre_id) values (3, 2);
insert into movies_genres (movie_id, genre_id) values (3, 1);
insert into movies_genres (movie_id, genre_id) values (4, 4);
insert into movies_genres (movie_id, genre_id) values (4, 1);
insert into movies_genres (movie_id, genre_id) values (4, 5);
insert into movies_genres (movie_id, genre_id) values (5, 3);
insert into movies_genres (movie_id, genre_id) values (5, 6);
insert into movies_genres (movie_id, genre_id) values (5, 1);
insert into movies_genres (movie_id, genre_id) values (6, 2);
insert into movies_genres (movie_id, genre_id) values (6, 1);
insert into movies_genres (movie_id, genre_id) values (7, 2);
insert into movies_genres (movie_id, genre_id) values (7, 1);
insert into movies_genres (movie_id, genre_id) values (8, 2);
insert into movies_genres (movie_id, genre_id) values (8, 1);
insert into movies_genres (movie_id, genre_id) values (9, 1);
insert into movies_genres (movie_id, genre_id) values (10, 3);
insert into movies_genres (movie_id, genre_id) values (10, 6);
insert into movies_genres (movie_id, genre_id) values (10, 1);
insert into movies_genres (movie_id, genre_id) values (11, 3);
insert into movies_genres (movie_id, genre_id) values (11, 6);
insert into movies_genres (movie_id, genre_id) values (11, 7);
insert into movies_genres (movie_id, genre_id) values (12, 1);
insert into movies_genres (movie_id, genre_id) values (12, 8);
insert into movies_genres (movie_id, genre_id) values (13, 3);
insert into movies_genres (movie_id, genre_id) values (13, 6);
insert into movies_genres (movie_id, genre_id) values (13, 1);
insert into movies_genres (movie_id, genre_id) values (14, 6);
insert into movies_genres (movie_id, genre_id) values (14, 9);
insert into movies_genres (movie_id, genre_id) values (15, 10);
insert into movies_genres (movie_id, genre_id) values (15, 3);
insert into movies_genres (movie_id, genre_id) values (15, 6);
insert into movies_genres (movie_id, genre_id) values (16, 6);
insert into movies_genres (movie_id, genre_id) values (16, 1);
insert into movies_genres (movie_id, genre_id) values (16, 7);
insert into movies_genres (movie_id, genre_id) values (17, 4);
insert into movies_genres (movie_id, genre_id) values (17, 2);
insert into movies_genres (movie_id, genre_id) values (17, 1);
insert into movies_genres (movie_id, genre_id) values (18, 3);
insert into movies_genres (movie_id, genre_id) values (18, 7);
insert into movies_genres (movie_id, genre_id) values (19, 1);
insert into movies_genres (movie_id, genre_id) values (20, 3);
insert into movies_genres (movie_id, genre_id) values (20, 6);
insert into movies_genres (movie_id, genre_id) values (20, 11);
insert into movies_genres (movie_id, genre_id) values (21, 2);
insert into movies_genres (movie_id, genre_id) values (21, 1);
insert into movies_genres (movie_id, genre_id) values (21, 12);
insert into movies_genres (movie_id, genre_id) values (22, 2);
insert into movies_genres (movie_id, genre_id) values (22, 1);
insert into movies_genres (movie_id, genre_id) values (22, 13);
insert into movies_genres (movie_id, genre_id) values (23, 10);
insert into movies_genres (movie_id, genre_id) values (23, 6);
insert into movies_genres (movie_id, genre_id) values (23, 14);
insert into movies_genres (movie_id, genre_id) values (24, 1);
insert into movies_genres (movie_id, genre_id) values (24, 15);
insert into movies_genres (movie_id, genre_id) values (25, 2);
insert into movies_genres (movie_id, genre_id) values (25, 1);
insert into movies_genres (movie_id, genre_id) values (25, 11);
insert into movies_genres (movie_id, genre_id) values (26, 3);
insert into movies_genres (movie_id, genre_id) values (26, 6);
insert into movies_genres (movie_id, genre_id) values (26, 11);
insert into movies_genres (movie_id, genre_id) values (27, 2);
insert into movies_genres (movie_id, genre_id) values (27, 1);
insert into movies_genres (movie_id, genre_id) values (28, 3);
insert into movies_genres (movie_id, genre_id) values (28, 7);
insert into movies_genres (movie_id, genre_id) values (29, 16);
insert into movies_genres (movie_id, genre_id) values (29, 1);
insert into movies_genres (movie_id, genre_id) values (29, 8);
insert into movies_genres (movie_id, genre_id) values (30, 1);
insert into movies_genres (movie_id, genre_id) values (30, 14);
insert into movies_genres (movie_id, genre_id) values (30, 11);
insert into movies_genres (movie_id, genre_id) values (31, 3);
insert into movies_genres (movie_id, genre_id) values (31, 1);
insert into movies_genres (movie_id, genre_id) values (32, 3);
insert into movies_genres (movie_id, genre_id) values (32, 1);
insert into movies_genres (movie_id, genre_id) values (32, 13);
insert into movies_genres (movie_id, genre_id) values (33, 4);
insert into movies_genres (movie_id, genre_id) values (33, 1);
insert into movies_genres (movie_id, genre_id) values (33, 5);
insert into movies_genres (movie_id, genre_id) values (34, 1);
insert into movies_genres (movie_id, genre_id) values (34, 17);
insert into movies_genres (movie_id, genre_id) values (35, 18);
insert into movies_genres (movie_id, genre_id) values (35, 7);
insert into movies_genres (movie_id, genre_id) values (36, 3);
insert into movies_genres (movie_id, genre_id) values (36, 6);
insert into movies_genres (movie_id, genre_id) values (36, 1);
insert into movies_genres (movie_id, genre_id) values (37, 18);
insert into movies_genres (movie_id, genre_id) values (37, 13);
insert into movies_genres (movie_id, genre_id) values (37, 12);
insert into movies_genres (movie_id, genre_id) values (38, 6);
insert into movies_genres (movie_id, genre_id) values (38, 16);
insert into movies_genres (movie_id, genre_id) values (38, 7);
insert into movies_genres (movie_id, genre_id) values (39, 2);
insert into movies_genres (movie_id, genre_id) values (39, 1);
insert into movies_genres (movie_id, genre_id) values (39, 12);
insert into movies_genres (movie_id, genre_id) values (40, 1);
insert into movies_genres (movie_id, genre_id) values (40, 12);
insert into movies_genres (movie_id, genre_id) values (41, 1);
insert into movies_genres (movie_id, genre_id) values (41, 13);
insert into movies_genres (movie_id, genre_id) values (41, 7);
insert into movies_genres (movie_id, genre_id) values (42, 3);
insert into movies_genres (movie_id, genre_id) values (42, 2);
insert into movies_genres (movie_id, genre_id) values (42, 1);
insert into movies_genres (movie_id, genre_id) values (43, 1);
insert into movies_genres (movie_id, genre_id) values (43, 9);
insert into movies_genres (movie_id, genre_id) values (44, 2);
insert into movies_genres (movie_id, genre_id) values (44, 1);
insert into movies_genres (movie_id, genre_id) values (45, 10);
insert into movies_genres (movie_id, genre_id) values (45, 6);
insert into movies_genres (movie_id, genre_id) values (45, 1);
insert into movies_genres (movie_id, genre_id) values (46, 2);
insert into movies_genres (movie_id, genre_id) values (46, 1);
insert into movies_genres (movie_id, genre_id) values (46, 13);
insert into movies_genres (movie_id, genre_id) values (47, 4);
insert into movies_genres (movie_id, genre_id) values (47, 1);
insert into movies_genres (movie_id, genre_id) values (47, 17);
insert into movies_genres (movie_id, genre_id) values (48, 4);
insert into movies_genres (movie_id, genre_id) values (48, 16);
insert into movies_genres (movie_id, genre_id) values (48, 1);
insert into movies_genres (movie_id, genre_id) values (49, 1);
insert into movies_genres (movie_id, genre_id) values (49, 8);
insert into movies_genres (movie_id, genre_id) values (49, 15);
insert into movies_genres (movie_id, genre_id) values (50, 13);
insert into movies_genres (movie_id, genre_id) values (50, 12);
insert into movies_genres (movie_id, genre_id) values (51, 9);
insert into movies_genres (movie_id, genre_id) values (52, 10);
insert into movies_genres (movie_id, genre_id) values (52, 1);
insert into movies_genres (movie_id, genre_id) values (52, 15);
insert into movies_genres (movie_id, genre_id) values (53, 1);
insert into movies_genres (movie_id, genre_id) values (53, 8);
insert into movies_genres (movie_id, genre_id) values (54, 16);
insert into movies_genres (movie_id, genre_id) values (54, 1);
insert into movies_genres (movie_id, genre_id) values (54, 8);
insert into movies_genres (movie_id, genre_id) values (55, 16);
insert into movies_genres (movie_id, genre_id) values (55, 1);
insert into movies_genres (movie_id, genre_id) values (55, 8);
insert into movies_genres (movie_id, genre_id) values (56, 1);
insert into movies_genres (movie_id, genre_id) values (56, 18);
insert into movies_genres (movie_id, genre_id) values (57, 10);
insert into movies_genres (movie_id, genre_id) values (57, 6);
insert into movies_genres (movie_id, genre_id) values (57, 1);
insert into movies_genres (movie_id, genre_id) values (58, 2);
insert into movies_genres (movie_id, genre_id) values (58, 1);
insert into movies_genres (movie_id, genre_id) values (58, 12);
insert into movies_genres (movie_id, genre_id) values (59, 10);
insert into movies_genres (movie_id, genre_id) values (59, 3);
insert into movies_genres (movie_id, genre_id) values (59, 6);
insert into movies_genres (movie_id, genre_id) values (60, 6);
insert into movies_genres (movie_id, genre_id) values (60, 1);
insert into movies_genres (movie_id, genre_id) values (60, 15);
insert into movies_genres (movie_id, genre_id) values (61, 3);
insert into movies_genres (movie_id, genre_id) values (61, 6);
insert into movies_genres (movie_id, genre_id) values (61, 1);
insert into movies_genres (movie_id, genre_id) values (62, 3);
insert into movies_genres (movie_id, genre_id) values (62, 6);
insert into movies_genres (movie_id, genre_id) values (62, 7);
insert into movies_genres (movie_id, genre_id) values (63, 1);
insert into movies_genres (movie_id, genre_id) values (63, 13);
insert into movies_genres (movie_id, genre_id) values (63, 15);
insert into movies_genres (movie_id, genre_id) values (64, 3);
insert into movies_genres (movie_id, genre_id) values (64, 1);
insert into movies_genres (movie_id, genre_id) values (64, 12);
insert into movies_genres (movie_id, genre_id) values (65, 3);
insert into movies_genres (movie_id, genre_id) values (65, 1);
insert into movies_genres (movie_id, genre_id) values (65, 13);
insert into movies_genres (movie_id, genre_id) values (66, 13);
insert into movies_genres (movie_id, genre_id) values (66, 12);
insert into movies_genres (movie_id, genre_id) values (67, 1);
insert into movies_genres (movie_id, genre_id) values (67, 12);
insert into movies_genres (movie_id, genre_id) values (67, 15);
insert into movies_genres (movie_id, genre_id) values (68, 3);
insert into movies_genres (movie_id, genre_id) values (68, 6);
insert into movies_genres (movie_id, genre_id) values (68, 7);
insert into movies_genres (movie_id, genre_id) values (69, 3);
insert into movies_genres (movie_id, genre_id) values (69, 6);
insert into movies_genres (movie_id, genre_id) values (70, 10);
insert into movies_genres (movie_id, genre_id) values (70, 1);
insert into movies_genres (movie_id, genre_id) values (70, 11);
insert into movies_genres (movie_id, genre_id) values (71, 4);
insert into movies_genres (movie_id, genre_id) values (71, 1);
insert into movies_genres (movie_id, genre_id) values (71, 17);
insert into movies_genres (movie_id, genre_id) values (72, 16);
insert into movies_genres (movie_id, genre_id) values (72, 1);
insert into movies_genres (movie_id, genre_id) values (73, 10);
insert into movies_genres (movie_id, genre_id) values (73, 6);
insert into movies_genres (movie_id, genre_id) values (73, 14);
insert into movies_genres (movie_id, genre_id) values (74, 1);
insert into movies_genres (movie_id, genre_id) values (74, 13);
insert into movies_genres (movie_id, genre_id) values (74, 12);
insert into movies_genres (movie_id, genre_id) values (75, 1);
insert into movies_genres (movie_id, genre_id) values (76, 16);
insert into movies_genres (movie_id, genre_id) values (76, 15);
insert into movies_genres (movie_id, genre_id) values (77, 1);
insert into movies_genres (movie_id, genre_id) values (77, 15);
insert into movies_genres (movie_id, genre_id) values (78, 1);
insert into movies_genres (movie_id, genre_id) values (78, 19);
insert into movies_genres (movie_id, genre_id) values (79, 2);
insert into movies_genres (movie_id, genre_id) values (79, 1);
insert into movies_genres (movie_id, genre_id) values (79, 13);
insert into movies_genres (movie_id, genre_id) values (80, 1);
insert into movies_genres (movie_id, genre_id) values (80, 15);
insert into movies_genres (movie_id, genre_id) values (81, 16);
insert into movies_genres (movie_id, genre_id) values (81, 1);
insert into movies_genres (movie_id, genre_id) values (81, 15);
insert into movies_genres (movie_id, genre_id) values (82, 2);
insert into movies_genres (movie_id, genre_id) values (82, 1);
insert into movies_genres (movie_id, genre_id) values (82, 13);
insert into movies_genres (movie_id, genre_id) values (83, 1);
insert into movies_genres (movie_id, genre_id) values (84, 1);
insert into movies_genres (movie_id, genre_id) values (85, 1);
insert into movies_genres (movie_id, genre_id) values (85, 8);
insert into movies_genres (movie_id, genre_id) values (86, 1);
insert into movies_genres (movie_id, genre_id) values (86, 8);
insert into movies_genres (movie_id, genre_id) values (86, 7);
insert into movies_genres (movie_id, genre_id) values (87, 6);
insert into movies_genres (movie_id, genre_id) values (87, 7);
insert into movies_genres (movie_id, genre_id) values (88, 4);
insert into movies_genres (movie_id, genre_id) values (88, 1);
insert into movies_genres (movie_id, genre_id) values (88, 5);
insert into movies_genres (movie_id, genre_id) values (89, 1);
insert into movies_genres (movie_id, genre_id) values (90, 2);
insert into movies_genres (movie_id, genre_id) values (90, 1);
insert into movies_genres (movie_id, genre_id) values (91, 2);
insert into movies_genres (movie_id, genre_id) values (91, 12);
insert into movies_genres (movie_id, genre_id) values (92, 10);
insert into movies_genres (movie_id, genre_id) values (92, 6);
insert into movies_genres (movie_id, genre_id) values (92, 16);
insert into movies_genres (movie_id, genre_id) values (93, 6);
insert into movies_genres (movie_id, genre_id) values (93, 4);
insert into movies_genres (movie_id, genre_id) values (93, 1);
insert into movies_genres (movie_id, genre_id) values (94, 3);
insert into movies_genres (movie_id, genre_id) values (94, 6);
insert into movies_genres (movie_id, genre_id) values (94, 11);
insert into movies_genres (movie_id, genre_id) values (95, 10);
insert into movies_genres (movie_id, genre_id) values (95, 3);
insert into movies_genres (movie_id, genre_id) values (95, 6);
insert into movies_genres (movie_id, genre_id) values (96, 16);
insert into movies_genres (movie_id, genre_id) values (96, 20);
insert into movies_genres (movie_id, genre_id) values (96, 8);
insert into movies_genres (movie_id, genre_id) values (97, 10);
insert into movies_genres (movie_id, genre_id) values (97, 6);
insert into movies_genres (movie_id, genre_id) values (97, 16);
insert into movies_genres (movie_id, genre_id) values (98, 1);
insert into movies_genres (movie_id, genre_id) values (98, 13);
insert into movies_genres (movie_id, genre_id) values (99, 16);
insert into movies_genres (movie_id, genre_id) values (99, 1);
insert into movies_genres (movie_id, genre_id) values (99, 8);
insert into movies_genres (movie_id, genre_id) values (100, 1);
```
