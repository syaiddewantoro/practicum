# Ice Game Store (Integrated Project 1).
We work at the online store "Ice," which sells video games from around the world. Data regarding user and expert reviews of games, genres, platforms (e.g., Xbox or PlayStation), and historical game sales data is available from open sources. We need to identify the patterns that determine whether a game is successful or not. That way, we can find the games with the most potential and plan their advertising campaigns.

We have data from 2016. We imagine that it is December of 2016, and we are planning a campaign for 2017.
This dataset contains abbreviations. ESRB stands for Entertainment Software Rating Board, which is an independent regulatory organization that evaluates game content and gives an age rating such as "Teen" or "Mature."

**Goals :**

1. Find the patterns that indicate whether a game is successful or not.
2. Finding sales variations for each game platform when a new platform appears, grows, and then decreases in popularity.
3. Determine the data collection period to forecast sales in 2017.
4. Determine which platforms generate the most sales and which platforms generate the highest profits.
5. Find out whether critic reviews and user reviews can influence the sales of a platform.
6. Find the most profitable genre.
7. Identifying user characteristics based on platforms, genres, and ratings and determining their impact on game sales.

**Hypothesis testing:**

- The average user rating for the Xbox One and PC platforms is the same.
- The average user rating for the action and sports genres is different.

# Results and Consclusion

**1. Data Preparation**

- To begin, we have a dataset with **16715** rows and **11** columns.
- Several columns have *missing values* such as the `Name`, `Year_of_Release`, `Genre`, `Critic_Score`, `User_Score`, and `Rating` columns. 
- We will change the case of column names and column value names to lowercase to make analysis easier.
- We change the `release_year` and `user_score` column types to the appropriate types.
- No duplicates were found.

**2. Transformation Data** 

- We create a new column called `global_sales` to calculate total sales from all over the world.
- We filter data from **2013** to predict sales in **2017**.

**3. Analytics and Data Visualization**

- From **1980** to **1994**, very few games were released because there were few platforms available; after **1994** and so on, many games were launched every year, reaching a *peak* in the period from **2005** to **2011**; after **2011**, the number of games launched began to decline; the reason could be that the old platform was beginning to be abandoned and users switched to a new, more modern platform; thus, many companies stopped releasing games.
- We know the top **6** platforms, namely: **ps2**, **x360**, **ps3**, **wii**, **ds**, and **ps**. Each platform has an average *lifespan* of **10** years; peak sales occur after **5** years of platform launch before declining; and manufacturers release their *next-generation* platform after **5** years of platform launch.We use 2013 data because that is when a platform begins to grow and reaches its peak sales.Since 2013, the PlayStation 4 has been the most popular platform. Then there are **ps3**, **x360** but the sales figures for the two platforms have greatly decreased to near **0**, then there are **3ds** which generate quite high sales even though these platforms show a declining sales trend since **2013**. The **ps4** and **xone** platforms should be on their way to peak game sales by now, we can ignore **2016** as it's not complete yet. 
- We find that `critic_score` does not affect the sales of a game, whereas `user_score` indicates an influence on sales although not too significant.The **ps3**, **x360**, and **ps4** platforms consistently produced the highest sales figures of the games we tested, but keep in mind that sales figures for the **ps3** and **x360** have decreased significantly.
- The top five sales genres are "action," "shooter," "sports," "role-playing," and "miscellaneous." However, because there are so many action games, the average price per game is not very profitable, so it is best to sell only popular titles in the "action" genre.

**4. Characteristics of Users in each Region**

- Users in the **NA** and **EU** regions share similar characteristics; they prefer **ps4**, **xone**, **x360**, **ps3**, and **platforms 3ds**, whereas in the **JP** region, which has its own characteristics, more users prefer the **3ds** platform, so that **ps4** ranks only **4** of the most popular platforms.
- Users in the **NA** and **EU** regions also have similar characteristics in their genre groups such as **action**, **shooter**, **sports**, and **role-playing**, whereas in the **JP** region they favor the **role-playing** and **action** genres and have little sales in other genres.
- Users in the **NA** region and **EU** region have similar characteristics, they mostly come from the **Mature/17+** age group, while for the **JP** region, more users come from the **Teen/ 13+**. So, **ESRB** ratings can affect game sales in a region. 

**5. Statistical Hypothesis Testing**
- The results of the first hypothesis show that the average `user_score` between **xbox one** and **pc** platforms is the same. This shows that the platform does not affect user satisfaction with a game.
- The second hypothesis reveals that the average `user_score` of the **action** and **sports** genres is different. This shows that the genre of a game can affect user satisfaction in buying a game.

**6. Recommendation**

- Based on the results of the analysis that we have done, we can provide recommendations to sell more games for the PS4 and Xbox One platforms because we can predict that these two platforms will reach peak sales in the next 1-2 years. For the 3DS platform, it can still generate sales for next year, but we have to reduce the supply.
- For the North America and Europe regions, the games with the most potential come from the Action genre in the Mature category, while in the Japan region we will get more sales from games in the Role-Playing genre and the Teen category.
