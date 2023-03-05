# Collaborative-Food-Recipe-Recommendation-System (Item Based)
This is a python script that uses collaborative filtering to recommend recipes to users based on their past ratings of other recipes. The script reads in two CSV files, RAW_interactions.csv and RAW_recipes.csv, containing information about recipe interactions and recipe details respectively. It filters and merges the two dataframes to get genuine users and famous recipes.

The script then performs train-test split on the final ratings dataframe and creates a pivot table for the train data. It calculates similarity scores between recipes using cosine similarity and predicts the rating for unrated recipes using user ratings and similarity scores. The top k recommendations are then returned for each user.

To evaluate the recommendation system, the script calculates precision and recall for different values of k and plots the scores against k using matplotlib.

## Dependencies
* pandas
* numpy
* scikit-learn

## Usage
To run the script, you need to have the RAW_interactions.csv and RAW_recipes.csv files in the specified location. You can change the test size and k-values as per your requirement.

## Author
(Data Demystifiers)
