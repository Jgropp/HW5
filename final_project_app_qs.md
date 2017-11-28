# SI 364 - Final Project questions

## Overall

* **What's a one-two sentence description of what your app will do?**

My app will take a Google Map API, and a Crimestop API and will allow the user to type in an area code, and in return they will see a map with all of 
the crimes that happened in that area code within the past week

## The Data

* **What data will your app use? From where will you get it? (e.g. scraping a site? what site? -- careful not to run it too much. An API? Which API?)**
Google Map API & Crimestop API

* **What data will a user need to enter into a form?**
US Zip Code

* **How many fields will your form have? What's an example of some data user might enter into it?**
The form will have two fields, one for the map with the crimes on it, and one with more detail about the crime 

* **After a user enters data into the form, what happens? Does that data help a user search for more data? Does that data get saved in a database? Does that determine what already-saved data the user should see?**
After a user enters data into the form, the Zip Code will be saved to one DB and their email will be saved to a differnet DB

* **What models will you have in your application?**
US Zip Code, Crimestop, SearH, User

* **What fields will each model have?**
User - Email Zip Code - ZC_ID, Crimesstop - CS_ID, ZC_ID Search - ZC_ID, CS_ID, Email

* **What uniqueness constraints will there be on each table? (e.g. can't add a song with the same title as an existing song)**
Can't look up anything outside of the United States, Can't have two of the same email, Only shows crime within the last week

* **What relationships will exist between the tables? What's a 1:many relationship between? What about a many:many relationship?**
(Zip - Crime, 1 to many), (Zip - Search, Many to many), (Crime - Search- Many to Many)

* **How many get_or_create functions will you need? In what order will you invoke them? Which one will need to invoke at least one of the others?**
1.Users
2.Zip
3.Crime

Search will invoke Zip
 
## The Pages

* **How many pages (routes) will your application have?**
3

* **How many different views will a user be able to see, NOT counting errors?**
3

* **Basically, what will a user see on each page / at each route? Will it change depending on something else -- e.g. they see a form if they haven't submitted anything, but they see a list of things if they have?**
(/) - submit buttons for email, zipcode, 
(/results) - Shows crime in past week for zipcode entered 
(/crime_map) A map showing all exactly where the crimes were in the past week for the zip entered




## Extras

* **Why might your application send email?**

To give a list of all the crimes every sunday for the past week

* **If you plan to have user accounts, what information will be specific to a user account? What can you only see if you're logged in? What will you see if you're not logged in -- anything?**

I am not having user accounts, only email for the purpose of sending the user crimes for the week if they want to

* **What are your biggest concerns about the process of building this application?**

making sure that the app is updaitng with crimes every day for the past week otherwise it will be outdated and not that helpful
