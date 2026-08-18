# FIFA World Cup 2026 Goal Prediction Challenge ⚽🏆

My solution to the **Zindi FIFA World Cup 2026 Goal Prediction Challenge**, where the objective was to predict both how many goals each team would score and how far they would progress in the 2026 FIFA World Cup.

**Final Ranking:** **34th out of 369 participants**
**Achievement:** 🥇 **Gold Medal — Top 10%**

## 🎯 The Challenge

The objective was to build a model that predicts:

1. The **total number of goals** each team would score during the FIFA World Cup 2026.
2. The **stage** at which each team would finish the tournament.

The challenge provided historical team-level records from FIFA Men's World Cup tournaments, sourced from the **Fjelstul World Cup Database**.

One of the things that made this challenge particularly difficult — and interesting — was the **closed-data restriction**.

Participants could only use the historical World Cup data provided by the competition. External datasets, pre-computed ratings, betting odds, web-scraped information, or other third-party data were not permitted.

Every useful signal therefore had to be **derived from the historical data itself**.

## ⏳ The Four-Year Problem

What made the challenge especially interesting was the structure of the data itself.

The World Cup is played only **once every four years**.

Unlike a typical sports prediction problem with weekly or seasonal data, the historical records contain large gaps between tournaments. A team's performance in one World Cup can be separated from its next observation by four years — enough time for squads, managers, tactics, form and overall team strength to change significantly.

This created an unusual temporal prediction problem:

> **How much can a team's past World Cup performance tell us about what it will do four years later?**

The challenge therefore wasn't simply about finding which teams had historically performed well. It was about determining **which historical signals were still relevant after a four-year gap**.

That made temporal feature engineering and understanding the progression of teams over multiple World Cups an important part of the modelling process.

## 🧠 Approach

I developed a machine learning approach combining:

* Historical World Cup data
* Time-aware feature engineering
* Recent performance and team trajectories
* Multi-task neural networks
* Random Forest modelling
* Poisson-based goal modelling
* Monte Carlo tournament simulation

The approach focused on extracting as much predictive information as possible from the limited historical data while accounting for the **four-year intervals between observations** and the unique **2026 World Cup format**.

## 📊 Evaluation

The competition used two evaluation metrics:

| Task             | Weight | Metric   |
| ---------------- | -----: | -------- |
| Goals Prediction |    60% | RMSE     |
| Stage Prediction |    40% | F1 Score |

The final leaderboard score combined both tasks into a single overall score.

## 🏆 Result

My final submission achieved:

public score 0.584492659
private score 0.557112414
This placed the solution in the **top 10% of the competition**.

The result was achieved under the competition's closed-data rules, using only the provided historical World Cup data and features derived from it.

## 🛠️ Tools & Technologies

* Python
* Pandas
* NumPy
* Scikit-learn
* PyTorch
* Machine Learning
* Feature Engineering
* Statistical Modelling
* Monte Carlo Simulation

## 📓 Implementation

The accompanying Jupyter Notebook contains the modelling pipeline, experimentation and final prediction workflow.

The repository focuses on the **challenge, modelling approach and competition result**, while the notebook provides the implementation details.

## 📚 Data Source

The historical data was provided through the competition and sourced from the **Fjelstul World Cup Database** by Joshua C. Fjelstul, Ph.D.

Data source: [https://github.com/jfjelstul/worldcup](https://github.com/jfjelstul/worldcup)

The dataset is licensed under **CC-BY-NC-SA 4.0**.

**Note:** Penalty shoot-out goals are not included in the target.

---

**Author:** Buumba Chinjila
**Competition:** Zindi — FIFA World Cup 2026 Goal Prediction Challenge
**Result:** 🥇 Rank 34th / 369
