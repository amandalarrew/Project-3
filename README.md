# Project 3: Advanced Running Retargeting Using NLP
---

## Overview

A running enthusiast mobile application company for all levels of runners was looking to launch a retargeting marketing campaign to convert advanced runners who have downloaded the application to being paid members. When the app is downloaded, users select their skill level. In an effort to understand their customer's needs, “Couch-to-5k (C25k)" and “Advanced Running” subreddits were analyzed and modeled using Natural Language Processing (NLP), Random Forest and Logistic Regression Classification Techniques. This project identifies the type of language being used between beginner and advanced runners and provides marketing retargeting ad recommendations for the advanced runners customer segmentation. 

"Couch to 5k" is a popular, free, beginner's running program by Josh Clark that helps non-runners become runners within 9 weeks. The program incorporates walking, running and cross-training into manageable increments, allowing those with little-to-no fitness level to start running. Not surprisingly, "Couch to 5k" has increased in popularity for beginner runners and has even become a popular subreddit for users to share tips, questions, wins and experiences with others as they begin their running journey. Advanced runners also use Reddit as a community for more advanced topics in running, such as marathon training, endurance running and race results. I used r/C25K and r/AdvancedRunning subreddits for NLP analysis in this project. 

The data used for this project are from the following sources: [r/C25K](https://www.reddit.com/r/C25K/), [r/AdvancedRunning](https://www.reddit.com/r/AdvancedRunning/).

---

## Contents
- [Part 1: Web-scraping](http://localhost:8888/files/code/part1_webscraping.ipynb?_xsrf=2%7C5edec799%7C1f952ed71739c1a862cf5f0c31e62217%7C1669644133)
- [Part 2: Initial Cleaning](http://localhost:8888/files/code/part2_cleaning.ipynb?_xsrf=2%7C5edec799%7C1f952ed71739c1a862cf5f0c31e62217%7C1669644133) 
- [Part 3: Preprocessing](http://localhost:8888/files/code/part3_preprocessing.ipynb?_xsrf=2%7C5edec799%7C1f952ed71739c1a862cf5f0c31e62217%7C1669644133) 
- [Part 4: EDA](http://localhost:8888/files/code/part4_eda.ipynb?_xsrf=2%7C5edec799%7C1f952ed71739c1a862cf5f0c31e62217%7C1669644133)
- [Part 5: Modeling and Conclusions](http://localhost:8888/files/code/part5_modeling_conclusions.ipynb?_xsrf=2%7C5edec799%7C1f952ed71739c1a862cf5f0c31e62217%7C1669644133)

---

## Summary of Findings and Recommendations 

The best model at predicting r/AdvancedRunning was the Balanced Logistic Regression Model. This model accounted for 92.09% variance in classifying the target variable. 

Some words that were predictive of r/AdvancedRunning were: 
- Posts containing "marathon" had a 3.69 increase in odds of being in r/AdvancedRunning. 
- Posts containing "pr" had a 2.09 increase in odds of being in r/AdvancedRunning. 
- Posts containing "mileage" had a 1.64 increase in odds of being in r/AdvanceRunning. 
- Posts containing "long run" had a 1.44 increase in odds of being in r/AdvancedRunning. 
- Posts containing "injury" had a 1.24 increase in odds of being in r/AdvancedRunning. 
- r/AdvancedRunning showed having higher odds of having positive, neutral and negative sentiment than r/C25K did. This explains more variation in sentiment across all posts. 

- Posts containing "c25k" had a 98% (1-0.14192) reduction in odds of being in r/AdvancedRunning.
- Posts containing "5K" had a 38% reduction in odds of being in r/AdvancedRunning. 
- Posts containing "Program" had a 36.67% reduction in odds of being in r/AdvancedRunning.
- Posts containing "start" had a 36.25% reduction in odds of being in r/AdvancedRunning.
- Posts containing "walk" had a 32.15% reduction in odds of being in r/AdvancedRunning. 
- Posts containing "stop" had a 21.84% reduction in odds of being in r/AdvancedRunning. 

Not surprisingly, seemingly more competitive words are predictive of being in r/AdvancedRunning. r/AdvancedRunning  predictive words are more optimization based, while r/C25K words are more completion based. Words predictive of being in r/C25k are more linked to beginning programs, shorter runs and walking. As a result, I recommend that re-targeting content for advanced runners should be aimed around tips for longer runs, how to get a pr in your next race, and how to prevent and deal with injury.  

I will continue to improve this project. I want to look more deeply into sentiment analysis after modeling, add a boosting model and clean up my vectorizing sections.

---
