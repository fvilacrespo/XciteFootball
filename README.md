# MatchPick
Final project for the Building AI course

## Summary

Describe briefly in 2-3 sentences what your project is about. About 250 characters is a nice length! 
This project uses AI to predict which football matches of the current gameweek will be the most entertaining and fun to watch. By analyzing historical stats like goal averages, big chances and play intensity, it ranks upcoming fixtures to help fans decide which games are worth watching.



## Background

Which problems does your idea solve? How common or frequent is this problem? What is your personal motivation? Why is this topic important or interesting?
Football fans often face a dilemma on weekends: there are too many matches and limited time to watch them. Often, we choose to watch a "big game" based on team reputation, only to be disappointed by a boring, defensive match, while missing a thrilling high-scoring game elsewhere.
* **Problem:** Time is wasted watching boring matches based on biased intuition or marketing. This can lead to viewer fatigue and a gradual decline in audience engagement over the long term.
* **Frequency:** Occurs every matchday (weekly) for millions of fans.
* **Personal Motivation:** As a football fan, I want to optimize my viewing time by prioritizing matches with the highest probability of action, goals, and intensity.
This project solves this by replacing intuition with data-driven probability.


## How is it used?

Describe the process of using the solution. In what kind situations is the solution needed (environment, time, etc.)? Who are the users, what kinds of needs should be taken into account?
The solution is designed for football fans who want to curate their weekend viewing schedule.
1.  **Input:** The system inputs the upcoming match fixtures for the week.
2.  **Processing:** The AI analyzes the recent form of both teams (goals scored/conceded, big chances created/conceded, defensive rigidity, style of play, etc.) from historical data.
3.  **Output:** The system assigns an "Excitement Score" or classifies the match into tiers (e.g., "Must Watch", "Solid Choice", "Likely Boring").



This is how you create code examples:
```
def main():
   countries = ['Denmark', 'Finland', 'Iceland', 'Norway', 'Sweden']
   pop = [5615000, 5439000, 324000, 5080000, 9609000]   # not actually needed in this exercise...
   fishers = [1891, 2652, 3800, 11611, 1757]

   totPop = sum(pop)
   totFish = sum(fishers)

   # write your solution here

   for i in range(len(countries)):
      print("%s %.2f%%" % (countries[i], 100.0))    # current just prints 100%

main()
```


## Data sources and AI methods
Where does your data come from? Do you collect it yourself or do you use data collected by someone else?
**Data Sources:**
* The primary data comes from [Football-Data.co.uk](https://www.football-data.co.uk/), which provides free historical CSV files for major European leagues (scores, shots, corners, fouls).
* In future versions, we might scrape data for more advanced metrics (like xG) from sites like FBref or Understat.
  
**AI Methods:**
* **Data Preprocessing:** Using Python (Pandas) to calculate rolling averages for teams (e.g., "Average goals scored in last 10 games").
* **Model:** We use **Linear Regression** (to predict the total number of goals) or a **Classification algorithm** (like K-Nearest Neighbors or Logistic Regression) to categorize matches into "High Fun" vs "Low Fun" based on a threshold.
* **Metrics:** The key feature is a custom "Fun Index" derived from goals, big chances, and lack of fouls/interruptions.


If you need to use links, here's an example:
[Twitter API](https://developer.twitter.com/en/docs)

| Syntax      | Description |
| ----------- | ----------- |
| Header      | Title       |
| Paragraph   | Text        |

## Challenges

What does your project _not_ solve? Which limitations and ethical considerations should be taken into account when deploying a solution like this?
While the model improves decision-making, it cannot predict the unpredictable nature of sports.

* **Unpredictable Events:** A red card in the 5th minute or a sudden injury can completely change the dynamic of a game, which pre-match statistics cannot foresee.
* **Subjectivity:** "Fun" is subjective. Some fans enjoy a tactical defensive battle (0-0), while this model prioritizes goals and offensive stats.
* **Ethical Considerations:** If this tool were used for gambling or betting, it would require strict disclaimers. This project is purely for entertainment purposes and optimizing leisure time, not for financial advice.

## What next?

How could your project grow and become something even more? What kind of skills, what kind of assistance would you  need to move on? 
This project has significant potential to grow from a simple course assignment into a robust data science portfolio piece.

* **Advanced Metrics:** Incorporating "Expected Goals" (xG) and "Expected Threat" (xT), or other advanced metrics, to refine the definition of quality play.
* **More data and parameters:** Processing larger datasets to include external variables—such as weather conditions, referee strictness, or historical rivalries—that significantly influence whether a match becomes dynamic or stagnant.
* **Web App:** Developing an app/web where users can check rankings from their phones without running Python code.
* **Skills Needed:** To achieve this, I will need to deepen my knowledge in Web Scraping, Time Series Analysis, and more advanced Machine Learning models. Also, **domain expertise** in football analytics is crucial to correctly perform feature selection and assign the right weight to the variables that truly matter.
  
## Acknowledgments
* Historical match data provided freely by [Football-Data.co.uk](https://www.football-data.co.uk/).
