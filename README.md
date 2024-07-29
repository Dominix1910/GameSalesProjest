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
Wii Sports

2.) Which year had the highest Sales?
2008

3.) Do any consoles seem to specialize in a particular genre based on top 5 consoles global sales.
DS console leads in Puzzle, Simulation, and Misc genre

PS2 console leads in the Fighting, Racing, and Sports Genre

The other 3 consoles are around the same level with the number of games released by genre.

4.) What titles are popular in one region but flop in another?

Grand Theft Auto V is very popular in NA and EU but not in Japan.

Only Pokemon Red/Blue is evenly popular in 3 regions 

Super Mario Bross and Tetris are only popular in NA compared to EU and JP

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


Link for Power Bi dashboard
[https://app.powerbi.com/view?r=eyJrIjoiNDA1ZjFmMGUtMTgzZi00YzgyLTkzYmUtOTJmNDI4ODVjODRmIiwidCI6IjZlZmQwZjIwLTU3YzgtNDQ0Ny1iNTNmLTAwZDQ5OTJjYTUwYiJ9
](https://app.powerbi.com/reportEmbed?reportId=adbda36b-50e3-4424-82a5-eafccd0af80b&autoAuth=true&ctid=6efd0f20-57c8-4447-b53f-00d4992ca50b)
