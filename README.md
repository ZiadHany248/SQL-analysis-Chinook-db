# SQL-analysis-Chinook-db

This is a SQL project conducted during a Udacity course

**Description:** This project is supposed to obtain data about various aspects of a database such as the money generated for each genre, the monney generated for each audio format and others. 
This project combines concepts such as `JOIN`, `GROUP BY` and nested queries to obtain the insights

**Functionality:** 
This project is divided into four insights:
- ### Insight No.1
_Subject:_ Which country has the most sales? What genre does this country sell the most?

_Conclusion:_ The country is The USA, they sell Rock music the most, it must also be noted that almost all countries sell rock music the most

_Code:_ Two temporary tables are created: `t1` which through a series of joins yields each track each customer bought belongs to, what it's cost was and to what coutnry it was shipped. We also create a second temporary table `t2` to choose the genre that sold the most from the `t1` using the aggreagte `MAX()`.
Finally, we `JOIN` `t1` and `t2` on a combination of the country and the maximum purchases to get the final result. This is how it looks
![This is an image](https://github.com/ZiadHany248/SQL-analysis-Chinook-db/blob/9b8bc499d093140b9d6d34b8a205e4c9933d7c34/first%20insight.png)



- ### Insight No.2
_Subject:_ Which artists has the most orders (number of orders)? Where do they get orders the most?

_Conclusion:_ The artist is Iron Maiden, they sell in america the most, it can be noticed that most artists sell the most in either America or Canada

_Code:_ Two temporary tables are created: `t1` which through a series of joins yields a table that contains the artist's name, the country to which their orders ship and the number of times an order shipped to that country. A second temporary table, `t2`, was created to choose the country that ordered the artist's tracks the most along with the name of the country 
Finally, we `JOIN` `t1` and `t2` on a combination of the country and the maximum number of orders to get the final result. This is how it looks
![This is an image](https://github.com/ZiadHany248/SQL-analysis-Chinook-db/blob/b364a8dd6e9282aa480c5f8d7db55fd30ef69b89/second%20insight.png)
_This visual only displays the top 50 artists_



- ### Insight No.3
_Subject:_ Which tracks were ordered the most?

_Conclusion:_ The track "The Troopers" was ordered the most. Although it must be noted that the difference is so marginal between the most ordered tracks that it may be best to deem this lead contingent

_Code:_ No temporary tables were required for this query. We select the track's name and use the aggregate `COUNT()` to count how many `InvoiceLine.Id` are regeistered under that track. We perform a couple of JOINs to put both tables together and get the result
This is how the end-result looks
![This is an image](https://github.com/ZiadHany248/SQL-analysis-Chinook-db/blob/2e129cabad83287c4dfca7a7359afeb604f1e31e/third%20insight.png)
_This visual only displays the only tracks with 3 or more orders_


- ### Insight No.4
_Subject:_ Does mediatype have an influence on sales?

_Conclusion:_ "MPEG Audio file" type generated the most revenue. There is a vast gap between the highest grossing type and the clossest one to it. This may be because All other types sound bad **or** because not many tracks are available in this format. This would require further investigation

_Code:_ This one required only one temporary table, also called `t1`.  It yields the type's name, the track's name and the total amount paid for it. 
Having derived that table, we sum the total money paid for each one of the types and `GROUP BY` each of the types. 
This is how the graph looks. It makes the huge gap between the highest grossing and all the others seem very clear
![This is an image](https://github.com/ZiadHany248/SQL-analysis-Chinook-db/blob/2e129cabad83287c4dfca7a7359afeb604f1e31e/fourth%20insight.png)

