This is a Portfolio project  (Work in progress)  

Author: Dominik Scibor

Website:

LinkedIn:

Introduction:

A portfolio project using dataset from kaggle

https://www.kaggle.com/datasets/gregorut/videogamesales



<b>Game Sales Report<b/>

Dataset used for this project with suggested questions.

![alt text](<Data source.png>)

In the first step, I used Excel to have a look at the data.

![alt text](<Excel data clearpng.png>)



Dataset loaded in Power Bi to clear and adjust.
The year column was changed from text to whole numbers.
![alt text](<powerbi query.png>)

Added new columns to transform Sales into millions.
![alt text](<power bi clear.png>)

Questions for this Dataset:

1.) Which Title sold the most Worldwide?
Wii Sports

2.) Which year had the highest Sales?
2008

3.) Do any consoles seem to specialize in a particular genre?
DS console leads in Puzzle, Simulation, and Misc genre

PS2 console leads in the Fighting, Racing, and Sports Genre

The other 3 consoles are around the same level with the number of games released by genre.

4.) What titles are popular in one region but flop in another?
Call of Duty: Black Ops 2

5.) Which region leads with game sales

6.) What genre gained the most sales?

Queries used:
Question 1
``` SQL
Select  Name, Global_Sales * 1000000 AS Sales
From vgsales
Order by Global_Sales Desc
Limit 1;
```
Question 2
``` SQL
Select round(sum(Global_Sales),2), Year
From vgsales
Group By Year
ORDER BY Global_Sales desc;
```
Link for Power Bi dashboard
https://app.powerbi.com/view?r=eyJrIjoiNDA1ZjFmMGUtMTgzZi00YzgyLTkzYmUtOTJmNDI4ODVjODRmIiwidCI6IjZlZmQwZjIwLTU3YzgtNDQ0Ny1iNTNmLTAwZDQ5OTJjYTUwYiJ9
