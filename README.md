How to:

1. Build a database in SQLite by downloading DB Browser and creating a database with it.

2. Write first a table that holds every unique item, and gives them an ID. Call it something like "ItemNames"

3. Write another table for each unique relationship between each unique item. Call it something like "Relationships"

4. Upload your database to an app builder such as FlutterFlow, that can work with a local SQLite database

5. Use this read query to get all unique items from the database:

	SELECT *
	FROM TABLE1;

6. You will need one overview page in the app that lists all unique items, and a profile page that dynamically fills text from the database such as the name and ID, which later is used to sort the database of unique relationships.

7. Make sure that the button on each listed database entry on the overview page, sends the unique ID of the item that is clicked, to the next page.

8. When the profile page is loading, run this query to make sure that it gets the right names and ID of each part in the relationship depending on the incoming ID to the page.
	This joins the ItemNames table with the Relationships table 

	SELECT ItemName, ItemB
	FROM Relationships 
	JOIN ItemNames
	ON Relationships.ItemB = ItemNames.ID 
	WHERE ItemA = ${ItemAID};

${}; is the syntax for the dynamic input variable

9. Make your app look nice and export the .apk to test it in your environment.
	(You can sign up for a free trial version for the subcription and that allows you to export the code)

10. Make sure that the wisdom and knowledge you are gathering, have validity and a use to be archived in a database


[Keep in mind that a rookie built this, so move forward with discretion]
