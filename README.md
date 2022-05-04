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
---

http://localhost:8000/cars/display?year=2001

will return all the cars with year 2001

---

http://localhost:8000/cars/display?make=Honda

will return all the cars with a make of Honda
---

http://localhost:8000/cars/display?make=Honda&year=2006

will return all the cars with a make of Honda and a year of 2006
---

http://localhost:8000/cars/display/id/128

will return the car with the id 128

---
http://localhost:8000/cars/display/rank/5

will return the car with a rank of 5

---
http://localhost:8000/cars/display/year/2001

will return the cars with a year of 2001
---
http://localhost:8000/cars/display/make/Honda

will return all the cars with a make of Honda
---

http://localhost:8000/cars/display/model/Accord

will return all the cars with a model of Accord

---
#Post API endpoints


http://localhost:8000/cars/register/json

along with a json object like
{
	"carid":-11,
	"carmake":"test",
	"carmodel":"test",
	"name":"test",
	"caryear":90,
	"email":"test"
}

Will add a record with the included values

The values are optional as I have -1 inserted if nothing is entered as a placeholder

year and id must be numbers or else an error occurs

---


http://localhost:8000/cars/register/query?carid=-11

will create a record with Car_ID -11 and add it to the database
you can also do other queries like

http://localhost:8000/cars/register/query?carid=-11&carmake=Test

This will also set the Car_Make


You do not use quotation marks and I have placeholders for values not entered

---


http://localhost:8000/cars/register/parameters/-11/testmake/testmodel/testemail/testname/-11


this will add a record with an id of -11 and a year of -11

The rest of the values say what they are for

They must be in the order shown

ID and year must be numbers


---

#Update API endpoints

http://localhost:8000/cars/update/json

with a json object like

{
	"carid":-11,
	"ranking":-90,
	"score":-70
}

Will update the record with id -11

an id must be given
if not I send a message

you do not need to update both 
If you update only ine the other will stay the same


---

http://localhost:8000/cars/update/query?carid=-11&ranking=-777

will update the ranking of the car with id -11

you can also use a query for score to change Total_Score

a carid must be given
I send a message if not provided


---


http://localhost:8000/cars/update/parameters/-11/100/0


will work on a car with id -11 and change the score to 100 and the ranking to 0

These must all be numbers and must all be there




