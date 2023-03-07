# Recommendation System Assignment-2

## Data
- The dataset used in this Assignment is the Food.com Recipes and Interactions dataset from Kaggle, which contains recipes and user interactions from the Food.com website. The dataset consists of two CSV files, one with recipe information and the other with user interaction information.

## General Steps:
- Preprocess data: preprocess the data and filter out irrelevant data, generate user-item rating matrix based on the data

- Choose a collaborative filtering algorithm: There are two main types of collaborative filtering algorithms: user-based and item-based. 

- Train the model: Use the chosen algorithm to train the model. This will involve identifying similarities between users or items based on the available data.

- Generate recommendations: Once the model has been trained, it can be used to generate recommendations for users. This could involve using the model to identify similar users or items to the ones that a user has already interacted with, and then recommending items that those similar users or items have also interacted with.

- Evaluate the model: To determine the accuracy of the model, use metrics such as precision, recall, and F1 score to evaluate its performance. This will help identify areas for improvement and ensure that the model is generating accurate recommendations.

## Files Overview:
1) EDA & Data Preprocessing.ipynb
- Insights from data and visualization 
- Toy-Data Generation [Quick Recipes]
- User-Item Rating pivot matrix generation


2) Matrix Factorization.ipynb
- Collaborative filtering based Recommendation system with Matrix Factorization (Model based - SVD)


3) Baseline_estimate.ipynb
- It is a model based collaborative recommendation system which is implemented from scratch by deriving equations from the research paper


4) MultiRound_Baseline.ipynb 
- Multi-Round Recommendation system based on Baseline estimation approach


5) Latent_Factor_Models.ipynb
- Recommedation system based on Latent Factor Model


6) Item_Item_Memory_Based.ipynb
- Item Item collborative Recommendation system without Matrix Factorization(Memory Based) 


7) Item_Item_Memory_Based-MRR(BASIC).ipynb
- Item Item collborative Multiround Recommendation system (Memory Based)


8) Item_Item_Memory_Based-MRR(DYNAMIC).ipynb
- Item Item collborative Multiround Recommendation system (Memory Based)


9) User_User_Memory_based_Recommendation_System.ipynb
- User User collborative Recommendation system (Memory Based)

## Contribution:
- There are 5 branches in this Repository :
- Main : Final Versions are pushed
- Vipasha : EDA, Data Preprocessing, Matrix Factorization Approaches with SVD (Single & Multiround RS)
- Sarvesh : Data Preprocessing, BaseLine Estimation, Latent Factor Model (Single & Multiround RS)
- Hiren: Item- Item based Collaborative Recommendations (Single & Multiround RS), webAPP deployment 
- Vedant: Data Preprocessing, User-User based Collaborative Recommendation system

## Online Web Application:
- we have made a  web app for recommendations with user interface that allows users to interact with a recommendation system and receive personalized recommendations.
- Link:https://github.com/thakkar-hiren/Collaborative-Recipe-Recommendation-System-Web-App

## We are currently working on the paper "Scalable Collaborative Filtering with Jointly Derived Neighborhood
Interpolation Weights"

* Interpolation of weights
$$\min_w J(w) = \sum_{(u,i) \in S_{tr}} (R_{u,i} - \hat{R}{u,i})^2 + \lambda \sum{j=1}^n w_j^2$$

$$\frac{\partial J(w)}{\partial w_j} = -2 \sum_{(u,i) \in S_{tr}} (R_{u,i} - \hat{R}{u,i}) R{u,j} + 2 \lambda w_j$$
$$w_j \leftarrow w_j - \alpha \frac{\partial J(w)}{\partial w_j}$$
$$w'j = \frac{\sum{v=1}^m S_{u,v} w_j}{\sum_{v=1}^m S_{u,v}}$$
$$\hat{r}{u,i} = \sum{j=1}^n w'j R{u,j}$$
