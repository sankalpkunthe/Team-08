# Team-08
Team 08 Task 03

This is program measures similarities between short captions. The goal is to identify similar captions, which is the base for recommandation systems like the proposed project.

At first I imported libraries like: *sentence_transformers* for embeddings, *torch* for tensor operations, *numpy* for numerical work, *re* for text cleaning, and *pandas* for displaying data neatly. A small helper function, *clean_caption()*, standardizes text by converting it to lowercase and removing URLs and special characters, ensuring clean input for the embedding model.

Now various captions covering topics like cats, cooking, football etc. is given as input. After cleaning, each caption is passed through the SentenceTransformer model 'all-MiniLM-L6-v2', which then converts text into token id {numerical value} stored in dense vector embeddings.

Next, the script calculates cosine similarity among all embeddings using util.cos_sim(). This metric quantifies how close two texts are in meaning, with 1 indicating strong similarity. The results are then stored and printed using pandas.

To make results more understandable, the script prints pairwise similarity scores, showing how related each caption is to every other. Finally, it includes best recommendation for every captions.
