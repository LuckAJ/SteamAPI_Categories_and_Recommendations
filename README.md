# **Recommendations per Category on Steam**
## Background
For this project, I wanted to learn how to call an API and then take that information and analyze it. I decided to look at Steam's API[^1] as I am interested in the video game industry. For this analysis, I want to investigate if there is a game category that gets more recommendations than any other category on the platform.
[^1]: Steam is a program where game developers and game artists can post their games for sale or for free, as some free-to-play game developers have done, and each person has their own account
## Data Collection
For this project, I wanted to use an API so that way I would have the most current data. I had some problems with getting it working as it was something new that I had never tried before. Using python, I made multiple functions that let me call Steam's API and then download all returned data as a CSV file. The function that I created to call the API was designed to time and limit my call requests in order to ensure I wouldn't overwhelm the API and get blocked from calling it during the project. I created an index file from SteamSpy's API, which allowed my function to grab data in batches reading the index file for reference as I was originally planning on using both SteamSpy and Steam data for this project.  One limiting factor that I discovered while working on this project was that SteamSpy's API was set up with pages which meant that I couldn't call to collect everything that they had. Ultimately, this meant that I only had a sample size of 1000 apps to work with and would be using Steam's data only for now. In the future, I would like to return to this project to review and explore additional questions using SteamSpy's information as well.

Check out my Jupyter Notebook including my API functions and the process of how I got my Data from the Steam API [here!](https://github.com/LuckAJ/SteamAPI_Categories_and_Recommendations/blob/main/Steam_Project_Collection.ipynb)
## Question: Is there a game category that gets more recommendations?
### Exploration
To start off, I want to get a sense of the data and explore how many games are categorized into each category that was available in the dataset. This information allowed me to have a baseline for the shape of the violin plot that I want to do for each category.

![Bar Graph for number of games](./Assets/Number_of_games_per_category.jpg)

In the sample, it is clear that there are more games in the Action category compared to the other categories such as Racing which had the lowest. This conclusion allows me to expect my violin to be wider than the Racing games for example. It is also interesting to see how popular Indie games have become with easier access to them.
### Answering the Question

Due to the limitations of my dataset,  my results are not necessarily representative of all the apps on Steam as a whole. To get more representative results to answer this question, I would gather a greater sample size. Which is something I hope to explore in the future of this project.

![Violin Graph for Rating Distribution](./Assets/Rating_distribution_by_category.jpg)

From this visualization, it is clear that games in the “Free-To-Play” category are not recommended by users to others to play very much. The top recommended game in this category does not reach as high as all other categories such as Action and RPG. Based on this analysis, I would recommend creating or investing in games in the Role-playing games (RPG) category as this game category has the overall highest recommended game, as well as most other games scoring higher recommendations higher than the median recommendations.

You can dive deeper into my code that was used to clean and complete this analysis as well as create my visualizations [here!](https://github.com/LuckAJ/SteamAPI_Categories_and_Recommendations/blob/main/Steam_Project.ipynb)

## Conclusion
For any game developers out there I would recommend creating a simulation game as the market is not as saturated and they are almost as highly recommended as RPGs. It would be easier to stand out and to get word of mouth from your players that would recommend it to others to help grow the player base.
