Schema: 

On the second table being created (public.cast_and_crew), probably shouldn’t default the name as “null” just so there’s no empty rows. 

In the public.liked_movies table, looking at the table schema alone, there could be possibility for the user to both like and dislike a movie. I could have missed it, but maybe this is made up for in the code. 

In a lot of the tables, the foreign key names are confusing, like “movie_genres_movie_id_fkey1”. 

For the public.movie_languages table, you could default the languages to something (like English?) instead of null. 

Also, in the Schema, I noticed the combined and joined tables from the backend API were not included. 

 

APIspec: 

In /movies/{movie_id}, there should be a request for the movie ID. 

In the /movies/new (POST) I noticed when creating a new movie, it requests an ID, but also returns that ID, maybe instead it can just return a confirmation.  

For /users/{user_id}/list/ (GET), we get the user’s list of movies, but without passing through some user verification. 

In /analytics/{movie_id}, I think there should be a request for the movie ID to pull its analytics. 

In /analytics/{genre}, same as the movie_id above, there should be a request for a genre ID to pull its analytics. 

In /predictions/{movie_id}, there should be a request for the specific movie ID. 

In /groups/{group_id}, it should request the group ID. 
