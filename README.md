# Multi-Table-Database-With-Relationships
Multi-Table Database With Relationships. Database populate  with tracks, artists, albums and genres.

# Demo 
All the data joined up sorted in ascending order by the album title

<img width="294" alt="DATABASE" src="https://user-images.githubusercontent.com/107360657/197580681-f62e86e5-de4e-45cd-b789-38f6f3f7dacd.png">

Query: 

'''SELECT Track.title as Song, Artist.name as Artist, Album.title Album, Genre.name as Genre
       FROM Track JOIN Genre JOIN Album JOIN Artist 
       ON Track.genre_id = Genre.genre_id AND Track.album_id = 
       Album.album_id AND Album.artist_id = Artist.artist_id
       group by Track.title ASC'''

# Buildt with the use of
- Primary key
- Logical key
- Foreing key

This table is a many-to-one relationship. Many tracks, there are many rows in the track table that point to the same album table.
