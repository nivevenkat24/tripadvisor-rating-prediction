README — TripAdvisor Rating Prediction (AI Studio)

Project Context
This project was completed as part of the course “Intro to AI and Application to Business” and focuses on predicting customer review ratings for TripAdvisor restaurant reviews using Altair AI Studio. The goal is to evaluate how different types of data—numeric ratings, text embeddings, and their combination—impact prediction accuracy and business usefulness.

Problem Statement (from HW 2)
Online platforms like TripAdvisor rely heavily on user reviews to measure customer satisfaction and guide decision-making. While star ratings provide a quick signal, they lack context, and written reviews contain rich information that is difficult to analyze at scale. The core problem is determining how to best leverage both structured numeric attributes and unstructured text data to accurately predict review ratings in a scalable and interpretable way.

Project Objective
The objective of this project is to build, compare, and evaluate multiple deep learning models to predict review_rating (1–5 stars) using:
1) Numeric restaurant and review attributes
2) Text embeddings generated from review content
3) A combined feature set of numeric attributes and embeddings

The project aims to answer:
- How much predictive power do numeric ratings alone provide?
- Do text embeddings improve prediction accuracy?
- Does combining structured and unstructured data outperform either approach alone?

Dataset
The project uses the TripAdvisor_2000 dataset, which contains:
- Review text (review_content)
- Overall review ratings (review_rating)
- Restaurant-level and review-level numeric attributes
The dataset is moderately sized and imbalanced toward higher ratings (4–5 stars), which impacts model performance.

Modeling Approach
The project is structured into three main modeling approaches:

1) Ratings-Based Model
A feedforward neural network trained only on numeric restaurant and review attributes. This serves as a baseline to understand how far structured data alone can go.

2) Embedding-Based Model
Review text is converted into 384-dimensional embeddings using FastEmbed (BAAI/bge-small-en-v1.5). A feedforward neural network is trained on embeddings only to capture semantic meaning from text.

3) Combined Model
Numeric attributes and text embeddings are merged into a single feature space and used to train a feedforward neural network. This model evaluates whether combining structured and unstructured data yields better predictive performance.

Each model is evaluated using classification accuracy and confusion matrices.

AI Studio Files
This folder contains exported AI Studio process files (.rmp), including:
- Embedding generation process
- Ratings-based neural network model
- Embedding-based neural network model
- Combined feature neural network model

Each process follows the standard AI Studio workflow:
Retrieve → Preprocess → Set Role → Split Data → Train Model → Apply Model → Performance Evaluation

Key Findings
- The ratings-only model achieved approximately 41% accuracy and was computationally lightweight.
- The embedding-only model improved accuracy to approximately 46.5%, capturing semantic information from text.
- The combined model achieved the highest accuracy at approximately 49%, demonstrating the value of blending structured and unstructured data.
- Performance was strongest for higher ratings, reflecting dataset imbalance.

Business Interpretation
From a business perspective, numeric ratings alone are insufficient to fully capture customer sentiment. Text embeddings add meaningful context but work best when anchored by structured data. The combined approach provides the most balanced and practical solution for platforms like TripAdvisor that need scalable, data-rich sentiment prediction.

If advising TripAdvisor as a consultant, the combined model would be recommended due to its higher accuracy and ability to leverage both quantitative signals and customer language.

How to Navigate This Folder
- Review the AI Studio process files (.rmp) to see each modeling pipeline
- Refer to class notes for theoretical background on embeddings and neural networks
- Use this README to understand the intent and structure before opening individual processes

Author
Nive Venkat
