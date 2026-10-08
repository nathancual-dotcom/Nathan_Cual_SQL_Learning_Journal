# Nathan_Cual_SQL_Learning_Journal_#2
Section 1: What I Learned 

What I learned was the basic on how to read, write and retrieve data using SQL. I was taught how to SELECT certain pieces of information and to properly filter them.  Through understanding both the Coding & Execution order of SQL coding I was able to utilize clauses identify WHERE within the dataset it is located, to use GROUP BY & ORDER BY to sort them by criteria and LIMIT to focus only on the necessary bits of data. The different clauses feed directly onto one another, SELECT is the data being looked for X, FROM is where X is stored, WHERE filters out the data until only data with X remains, GROUP BY than groups them based on categories while HAVING looks for the data X. ORDER BY than categorized them into a given categories while LIMIT is used to limit number of entries that are shown in the end result.

Section 2: A Query I Am Proud Of 

SELECT 	g.Name, 
        COUNT(t.TrackId) AS NumTracks
FROM genres g
JOIN tracks t ON g.GenreId = t.GenreId
GROUP BY g.Name
ORDER BY NumTracks DESC
LIMIT 5

I’m proud of this one as I was able to figure thus one out without heavily relying on additional AI tools. Since I’m looking got the “genre names” & “amount of tracks” I gan first search for the names in the “genres g” table than connect it to the “tracks t” table as they share the “GenreId” key. Since I used “g.Name” for the “SELECT” I had to use it for the “GROUP BY”. After that I used “ORDER BY” + “DESC” to arrange the final output as instructed. While I still needed to pinpoint what I was missing or what I did wrong, I was still able to correctly write and understand most of it before I needed to utilize AI assistance.  While this query still shows me that I lack proficiency in the usage SQL it also showed me that I already understood the fundamentals and can begin advancing to improve my skills in my own time. 


Section 3: A Mistake or Struggle  

SELECT 
	c.FirstName, c.LastName,
	(
		SELECT SUM(Total) FROM invoices i
		WHERE i.CustomerId = c.CustomerId
	) AS TotalSpent
FROM customers c
ORDER BY TotalSpent DESC
LIMIT 5

I had a hard time trying to map out which names to use and where to put them. I had to examine the customer and invoice tables separately, after finding a matching key in both tables, I could start searching for the “FirstName” and “LastName” of the customers. I then I made a subquery where the sum of the total sales found in the matching keys was totaled than renamed as TotalSpent. After that it was a matter of presenting the data in how the question asked it to. I it explanation sounds simple I had to rewatch video sessions and reread my notes repeatedly because I kept getting confused on the process and which tables to put were. This question to me was the first question that took marginally longer to solve.


Section 4: Connecting to the Real World  

My father’s friend works with a company that both manages and provides/supplies the inventory of perishable goods to several store. In that instance the encoding of official transaction and delivery records are all done using computers. While the digitation already allows for greater easy way to backup and access records in case of emergencies, the use of SQL would allow for greater ease of accessing select pieces of information. By using clauses like JOIN and the Aggregation Functions it would be able to bring up both all of a specific category an to look for specific orders. Through properly utilizing SQL it allows some to greatly streamline and cut down the amount of tie need to do certain tasks.

Section 5: Self-Assessment  

As of now I view my “Basic” understanding and my usage of “Aggregation” as the highest at 5 & 4-4.5 respectively. These concepts were pretty strait forward so I have no major problem in remembering the processes for the easy practice items. Regarding the usage of “Joins with 2, 3 or more table they are also relatively easy to understand but can be a little confusing with the introduction of linking separate tables. Because of this I would rate my current proficiency with them at 3-4. Conversely, I currently view my application of “Subqueries” and “CTEs” as my lowest at both 2-3. Queries that require either or both naturally take the most time and require additional tools.

Section 6: Goals and Next Steps

I still need further practice in in my general understanding of SQL, while can now understand how to read a SQL program and generally understand what it looking for, where its pulling from and what it doing with said data. It still takes me a while to figure out how to translate that into an SQL program with more complex prompts taking marginally more time for me to figure out. While I can still figure out how to write the code, I still takes me awhile and requires additional tools to point out my mistakes.
