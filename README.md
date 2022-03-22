# Problem Statement:
Design an algorithm that recommends course videos in a more efficient manner than other algorithms, removing redundant or useless information from an information stream before presenting it to a user, or more specifically, as a subclass of an information filtering system that attempts to predict the "rating" or "preference" a user will give to an item.

## Dataset
I am using Netflix Dataset.
I have provided the sample of the dataset above u can see it.
As the dataset is of size 2gb so its difficult to upload
Inside the download folder you will find two things 
a) first is the training_set folder which contains the text file in which movie id along with their rating and date of rating is given.
b) Second is movie_titles.txt it contains movie_id movie release date and movie name

## My solution
Dataset is of size 2gb and is containing lots of records.
if i will use pandas table for accessing the data then it would be slow as the data size is big and also
#### out of memory is the problem here because of the 2gb size of the data
  #### So my solution is to store the data into a python datastructure called dictionary
  In this dictionary movie_id is the key and movie ratings are the ratings which are stored in list

## Data Structures used are lists,dictionary.


## My recommendation model 
Suppose i want to get recommendation for the movie named NetForce.
1) First it will calculate the average ratings and ratings count of the movie NetForce by using the datastructure i have used which is dictionary
2) After that i will calculate average ratings and ratings count of other movies which are present in the training set
3) Now comes the main step which is calculating cosine similarity between the two vectors ,
In this case Vector A would be average ratings and ratings count for that particular movie and Vector B will be avg ratings and ratings counts of another movie
We will calculate the cosine similarity between these two movies and store the result
4) After looping through all the movies present inside trainig set, top 10 movies with highest similarity will be choosen and shown to the user.

### Thank you for reading 

