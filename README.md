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

`rating` has 731,927 rows and 5 columns.

| Column        | Description         |
| :------------ | :------------------ |
| `'user_id'`   | The unique identifer of the user who posted the review. (`int`)             |
| `'recipe_id'` | The recipe's unique identifier, same as `recipes`. (`int`)            |
| `'date'`      | The date the rating was posted. (`str`)   |
| `'rating'`    | The rating the user gave the recipe, 0-5, inclusive. (`int`)         |
| `'review'`    | The user's review. (`str`)        |


Since `rating` has many more rows than `recipe,` this means many recipes likely have multiple ratings. In order to see both the recipes and ratings together in one dataframe, we can merge them on a common column-here, we can use `id` (in `recipes`) and `recipe_id` (in `ratings`) as the columns to merge on.

Since we don't know if every recipe has at least one rating, however, so we'll make sure to use the parameter `how = 'left'` during the merge to keep all the recipes from the `recipes` dataframe.

Below is the first 5 rows of the merged dataframe, which initially has 243,429 rows and 17 columns. Since there are many columns I have just kept and displayed the ones most relevant to this project.

As per the instructions, I filled all ratings on 0 with np.nan. Since ratings are usually on a scale of 1-5 (inclusive), a rating of 0 suggests that the user just didn't input a rating. To avoid bias in the ratings, the value has been filled with 0. Additionally, an `average_rating` column has been added, containing the average rating per recipe. Since a recipe has many ratings from several users, the average of all ratings can show us the general approval of a given recipe. Since the `nutrition` column is actually a string and not a list, I have changed every value to a list by looping through every value in the series, splitting the string, and changing it to a float. 

| name                                 | minutes | nutrition             | n_steps | n_ingredients | rating | review                               | rating_avg |
|:------------------------------------|--------:|:--------------------|--------:|---------------:|-------:|:------------------------------------|-----------:|
| 1 brownies in the world ...          |      40 | [138.4, 10.0, 50.0...|      10 |              9 |      4 | These were pretty good, but...      |          4.0 |
| 1 in canada chocolate chip ...       |      45 | [595.1, 46.0, 211...|      12 |             11 |      5 | Originally I was gonna cut...       |          5.0 |
| 412 broccoli casserole               |      40 | [194.8, 20.0, 6.0...|       6 |              9 |      5 | This was one of the best...         |          5.0 |
| 412 broccoli casserole               |      40 | [194.8, 20.0, 6.0...|       6 |              9 |      5 | The photos you took (shapeweaver)...|           5.0 |
| 412 broccoli casserole               |      40 | [194.8, 20.0, 6.0...|       6 |              9 |      5 | Thanks so much for sharing...       |           5.0 |



# Data Cleaning and Exploratory Data Analysis

# Assessment of Missingness

# Hypothesis Testing 

# Framing a Prediction Problem

# Baseline Model

# Final Model

# Fairness Analysis
