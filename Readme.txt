How to run this script
1-Set up a ssh connection with your virtual machine with Putty
2-Make a directory for the data with this command "hadoop fs -mkdir data"
3-Downloading the u.data with this command "wget http://witan.nl/hadoop/u.data" 
4-Copy the data to your local folder with this command "hadoop fs -copyFromLocal u.data data/u.data"
5-Make a script in nano with this command "nano script name" and then add the code to the script
6-Run the script with python with command "python script_name data_file_path"



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
