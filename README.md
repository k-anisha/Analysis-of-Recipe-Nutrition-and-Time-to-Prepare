# An-Analysis-of-Recipe-Nutrition-and-Time-to-Prepare
This is a final project for DSC 80 at UCSD! Created by Anisha Kalgi.

# Introduction 
Hello! In this notebook I'd be exploring the **Recipes and Ratings** dataset. I picked this dataset because I love cooking--it's one of my biggest hobbies. As a college student, cooking healthy but time-efficient meals has been a growing responsibility this year, so I think it'd be interesting to work with data that pertains to me! The dataset also seems like it has the potential to have several interesting insights. 

Cooking healthy food can be rewarding but also feel like a chore--the time that it takes to chop veggies sometimes feels much more time consuming than, say, making a quick bowl of instant noodles or heating frozen pizza. **I wonder if there is a relationship between healthier recipes and the time it takes to make them.** To investigate this relationship, I am analyzing two datasets, one consisting of recipes posted since 2008 on food.com, and the other consisting of ratings for recipes posted since 2008 on food.com. The original purpose of the datasets is for the recommender system research paper, 'Generating Personalized Recipes from Historical User Preferences' by Majumder et al.

You can find the dataset [here](https://drive.google.com/drive/folders/1m_JXpgS2rR1-UYWAnffuUYiA50LvljF1).


## Exploring the Dataset ##
There are two datasets to consider here, `recipe` and `rating.` Let's take a look at both of them:

`recipe ` has 83,782 rows and 12 columns. The 12 columns in `recipe` are:

| Column             | Description                                                                                                                                                                                       |
| :----------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `'name'`           | The title of the recipe. (`str`)                                                                                                                                                                                       |
| `'id'`             | The recipe's unique identifier. (`int`)                                                                                                                                                                                        |
| `'minutes'`        | The minutes it takes to prepare the recipe. (`int`)                                                                                                                                                                       |
| `'contributor_id'` | The unique identifer of the user who submitted the recipe. (`int`)                                                                                                                                                                |
| `'submitted'`      | The date the recipe was submitted. (`str`)                                                                                                                                                                         |
| `'tags'`           | List of Food.com corresponding tags for the recipe. (list of `str`)                                                                                                                                                                     |
| `'nutrition'`      | Nutrition information, formatted as [calories, total fat as PDV, sugar as PDV, sodium as PDV, protein as PDV, saturated fat as PDV, carbohydrates as PDV] (`str`) 
| `'n_steps'`        | The number of steps in the recipe. (`int`)                                                                                                                                                                          |
| `'steps'`          | A list of the recipe steps in order. (list of `str`)                                                                                                                                                             |
| `'description'`    | The user-provided description of the recipe. (`str`)                                                                                                                                                                          |
| `'ingredients'`    | A list of the ingredients for the recipe. (list of `str`)                                                                                                                                                                      |
| `'n_ingredients'`  | The number of ingredients in the recipe. (`int`)                                                                                                                                                              |



# Data Cleaning and Exploratory Data Analysis

# Assessment of Missingness

# Hypothesis Testing 

# Framing a Prediction Problem

# Baseline Model

# Final Model

# Fairness Analysis
