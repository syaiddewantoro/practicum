<p align="center">
  <a href="https://practicum.com/id-idn/">
    <img src="https://github.com/syaiddewantoro/resources/blob/main/project%20image/music.jpg" alt="drawing" width="600" height="300">
  </a>
</p>

# Comparing Music Preferences Between Two Cities <a id='intro'></a>

## Basic Python
Whenever we do research, we need to formulate a hypothesis that we can then test. Sometimes we accept this hypothesis, but sometimes we also reject it. To make the right decisions, a business must be able to understand whether the assumptions it makes are correct or not.

In today's project, you will compare the musical preferences of the cities of Springfield and Shelbyville. You will study actual Y.Music data to test the hypotheses below and compare user behavior in these two cities.

## Objective:
Testing three hypotheses:
1. User activity varies depending on the day and city.
2. On Monday mornings, residents of Springfield and Shelbyville tune in to different genres. It also applies to Friday nights.
3. Listeners in Springfield and Shelbyville have different preferences. In Springfield, they prefer pop music, while in Shelbyville, rap music has more fans.

## Stages
Data about user behavior is stored in the file `/datasets/music_project_en.csv`. There needs to be more information about the data quality, so you need to check it before testing the hypothesis.

First, you will evaluate the quality of the data and see if the problem is significant. Then, during data pre-processing, you will try to account for the most severe issues.
 
The project will consist of three phases:
  1. Data overview
  2. Data pre-processing
  3. Test the hypothesis
  
 ## Findings

 We have tested the following three hypotheses:

1. User activity varies depending on the day and city.
2. On Monday mornings, residents of Springfield and Shelbyville tune in to different genres. It also applies to Friday nights.
3. Listeners in Springfield and Shelbyville have different preferences. In both Springfield and Shelbyville, they preferred pop music.

After analyzing the data, we can conclude:

1. User activity in Springfield and Shelbyville depends on the day, even if the city is different.

The first hypothesis can be entirely accepted.

2. Musical preferences were similar during a week in Springfield and Shelbyville. We can see a slight difference in the order on Monday, but:
* In both Springfield and Shelbyville, most people listen to pop music.

So we cannot accept this hypothesis. We also have to remember that the results could have been different were it not for the missing values.

3. The music preferences of users from Springfield and Shelbyville are very similar.

The third hypothesis is rejected. If there are differences in preference, it cannot be seen from this data.

### Notes
In real projects, research involves statistical hypothesis testing, which is more precise and more quantitative. Also, note that you can only sometimes conclude an entire city based on data from just one source.

You'll study hypothesis testing in the statistical data analysis sprint.
