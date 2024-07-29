This is a Portfolio project  

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

2.) Which year had the highest Sales?

3.) Do any consoles seem to specialize in a particular genre based on top 5 consoles global sales.

4.) What titles are popular in one region but flop in another?

5.) Which region leads with game sales

6.) What genre gained the most sales?

7.) Analysis of publishers.

Queries used:
Question 1
``` SQL
Select  Name, Global_Sales * 1000000 AS Sales
From vgsales
Order by Global_Sales Desc
Limit 1;
```
![image](https://github.com/user-attachments/assets/5357433f-5f4c-478d-9989-4644c1e4746a)

Question 2
``` SQL
Select round(sum(Global_Sales),2), Year
From vgsales
Group By Year
ORDER BY Global_Sales desc;
```
![image](https://github.com/user-attachments/assets/2bcafcda-ecb7-4057-9726-dff8181bc771)

Question 3


![image](https://github.com/user-attachments/assets/93c022ab-2529-49bf-9546-531f0136195d)

Question 4

![image](https://github.com/user-attachments/assets/a2549cb0-684d-4dcd-9405-020b3c8b2937)

Question 5

![image](https://github.com/user-attachments/assets/23dad7dc-33d0-4210-9da7-12a734e7e2e4)

Question 6

![image](https://github.com/user-attachments/assets/67fc8e70-ba15-4f06-99af-6dd02dca46df)

Question 7

![image](https://github.com/user-attachments/assets/ee86e18e-0d02-42b7-a9d7-ec0a059dd7d1)



Link for Power Bi dashboard
[https://app.powerbi.com/view?r=eyJrIjoiNDA1ZjFmMGUtMTgzZi00YzgyLTkzYmUtOTJmNDI4ODVjODRmIiwidCI6IjZlZmQwZjIwLTU3YzgtNDQ0Ny1iNTNmLTAwZDQ5OTJjYTUwYiJ9
](https://app.powerbi.com/reportEmbed?reportId=adbda36b-50e3-4424-82a5-eafccd0af80b&autoAuth=true&ctid=6efd0f20-57c8-4447-b53f-00d4992ca50b)
