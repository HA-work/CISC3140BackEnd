# CISC3140BackEnd
A repo for my work on Project 4

I was able to accomplish most of the work except for updating and adding multiple records at once.
I found no easy way to do this.


After copying the repo and having the relevant modules like express and nodemon you should only need to use npm start to start the server.

You should use either Insomniac or PostMan to interact with the server


#API Endpoints


#Get API endpoints

.http://localhost:8000/cars/display

This will return all of the records in the database

It has query capabilities for year and make

For make I edited the code so that you do not need to use quotation marks

http://localhost:8000/cars/display?year=2001

will return all the cars with year 2001

http://localhost:8000/cars/display?make=Honda

will return all the cars with a make of Honda


http://localhost:8000/cars/display?make=Honda&year=2006

will return all the cars with a make of Honda and a year of 2006


http://localhost:8000/cars/display/id/128

will return the car with the id 128


http://localhost:8000/cars/display/rank/5

will return the car with a rank of 5


http://localhost:8000/cars/display/year/2001

will return the cars with a year of 2001

http://localhost:8000/cars/display/make/Honda

will return all the cars with a make of Honda


http://localhost:8000/cars/display/model/Accord

will return all the cars with a model of Accord





