1) Gets a book review from the user, rating with a written review.
2) Pulls movies based on actors
3) Filters movies based on their duration



1) Book review (completely written by the user): /village/write_review  

curl -X 'POST' \ 'https://testinghosting-yyoz.onrender.com/village/write_review' \ -H 'accept: application/json' \ -H 'access_token: hlath' \ -H 'Content-Type: application/json' \ 

Request: { 

	“user_id”: int, 

	“rating”:int, 

	“review_text”: string # users can write in-depth review of their mocies 

} 

Response: “Okay” 

 

2) Pull similar movies by actors: /movies/similar/actors/{movie_id} GET 

curl -X 'GET' \ 'https://testinghosting-yyoz.onrender.com/movies/similar/by_actors/42' \ -H 'accept: application/json' \ -H 'access_token: hlath' \ -H 'Content-Type: application/json' 

Request: { 

"actor_id”: int	 

} 
Response: 

[{ 

"movie_id": "integer", 
  "name": "string", 
  "release_year": "integer", 
  "description": "str",  
  "average_rating": "integer", 
  "budget": "integer", 
  "box_office": "integer", 
  "languages": ["string"] 

	 

}] 

 

3) Filter movies  by duration: /movies/filter/duration GET 

Request: { 

	“min_duration”: int, 

	“max_duration”: int 

} 

 

Response:  

[{ 

"movie_id": "integer", 
  "name": "string", 
  "release_year": "integer", 
  "description": "str",  
  "average_rating": "integer", 
  "budget": "integer", 
  "box_office": "integer", 
  "languages": ["string"] 

	 

}] 
