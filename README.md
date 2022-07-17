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

