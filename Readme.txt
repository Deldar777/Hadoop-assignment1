Counting number of ratings per movie
1.	Mapper: the first step is the mapper. The 
function is going through the whole dataset and 
returning the movie id. For example, if you have movie 
number 400 two times and 500 three times then the result 
will be like this: 400,1 - 400,1 – 500,1 – 500,1 – 500, 1 etc. 
2.	The second step is the reducer: the reducer 
function like the name says is reducing the results 
by combining all the keys and increasing the value 
by one each time the same key is found. For Example,
 if we are going with the previous example the results 
would be something like this: 400,2 – 500,3 
