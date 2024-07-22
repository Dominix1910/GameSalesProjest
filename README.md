This is Portfolio projest    

Author: Dominik Scibor

Website:

LinkedIn:

Introduction:

A portfolio projest using dataset from kaggle

https://www.kaggle.com/datasets/gregorut/videogamesales



<b>Game Sales Report<b/>

Dataset used for this projest with suggested questions.

![alt text](<Data source.png>)

In first step I used Excel to have a look at the data.

![alt text](<Excel data clearpng.png>)



Dataset loaded in Power Bi to clear and adjust.
Year Column changed from text to whole number.
![alt text](<powerbi query.png>)

Added new columns to transform Sales into milions.
![alt text](<power bi clear.png>)

Questions for this Dataset:
1.) Which Title sold the most Worldwide?
2.) Which year had the highest Sales?
3.) Do any consoles seem to specialize in a particular genre?
4.) What titles are popular in one region but flop in another?
5.) Which region leads with game sales
6.) What genre gained most sales?

For first question I used MySQL

Select  Name, Global_Sales * 1000000 AS Sales
From vgsales
Order by Global_Sales Desc
Limit 1;