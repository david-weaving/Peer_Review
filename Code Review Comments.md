##users.py: 

In the user signup function, there could be an exception to handle a possible database connection error and rollback, but for the most part seems solid. 

In the user login function, there’s an unnecessary variable call with user_id = 0 

In the user list function, after obtaining results, you can pull the for loop out of the db connection call. 

##Recommendations.py: 

In the get recommended function, should be able to cut down the huge query with a simpler ‘Group By’. 

In the get recommended function, there are SQL calls within a for loop, this can cause problems and potentially miss some calls being made to/by the DB. 

In the format movies function, it would look cleaner if the variables were updated in the dictionary itself. 

##Predictions.py: 

In the create prediction function, you can again simplify the giant query by doing a WITH and making one big table. 

##Catalog.py: 

In the search movies function, you could drop the big if/else statement and condense it into a dictionary and use it as a map. 

##Analytics.py: 

In the get movie analytics function, the variables set to zero towards the top are unnecessary. 

In the get most popular function you can pull statements out of the database connection call. 

##Overall: 

There are a lot of if/else statements that make for bad code readability 

There’s also a lot of code that could be pulled out of the database connection call once you grab your variables. 
