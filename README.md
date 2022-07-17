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
![This is an image]([first insight.png](https://github.com/ZiadHany248/SQL-analysis-Chinook-db/blob/9b8bc499d093140b9d6d34b8a205e4c9933d7c34/first%20insight.png))
