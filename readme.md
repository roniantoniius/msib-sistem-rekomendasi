# Recommendation System for Internship Positions in the MSIB Program at Kampus Merdeka Indonesia

This project aims to develop a content-based recommendation system (Content Based Filtering) that can assist students in choosing positions or internship vacancies available at the MSIB Program at Merdeka Campus. By using vacancy data and position descriptions, this system tries to provide the most relevant recommendations based on the information provided by the user.

## Data Preparation
This project uses a Content Based Filtering approach, where recommendations are given based on the similarity between the description of the position selected by the user and other positions. This method involves several main steps, including:

- Data Preprocessing: Cleaning and preparing internship position description data using stemming techniques with the Sastrawi library.
- Vectorization: Converting the description text into a vector representation using CountVectorizer.
- Similarity Calculation: Calculates the similarity between positions using cosine similarity.


## Documentation
![image](https://github.com/roniantoniius/msib-sistem-rekomendasi/assets/121453378/47fa5c57-b8d9-40f1-a357-f8a0c74c3a47)

![image](https://github.com/roniantoniius/msib-sistem-rekomendasi/assets/121453378/aa709cf6-20d5-4672-b9f1-2da94b21294f)




## Conclusion for version 1
The recommendation system method with Content Based Filtering is not very suitable for recommending internship vacancies at MSIB Merdeka Campus. This is because there is some data such as `description` and `detail_description` which does not really explain about the internship position but explains about the project case that will be carried out. Both description variables are very detailed and long, so it is possible for other internship vacancies to have similar vector representations.

## Conclusion for version 2
The recommendation system by applying Content Based Filtering in this 2nd experiment has a slightly better performance when compared to the first experiment using `description` and `detail_description` data. This is probably because it only uses variables that discuss the internship position.

## Solution
- Deep dive understanding of the pattern of `description` and `detail_description` data. Then improve the data in the `tags` feature.
- Using other Vectorizer techniques.
- Direct survey to collect data about internship positions favored by other users. So that later we can apply Collaborative Filtering methods or techniques that will be more suitable than CBF.	

## How to run this repo
1. Download or Clone the repository.
2. I suggest to run the environment `.\env\Scripts\Activate`
3. Install the required libraries using `pip install -r requirements.txt`.
4. Run the Streamlit app using `streamlit run magang.py`.
5. Interact with the recommender system about intern msib
6. Or you guys can go to the deployed app:https://msib-sistem-rekomendasi.streamlit.app/
