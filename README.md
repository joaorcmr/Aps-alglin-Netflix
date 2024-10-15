# Netflix Movie Recommendation System Using SVD

This project is a demonstration of how Singular Value Decomposition (SVD) can be applied to build a simple recommendation system. The focus of this system is to predict user ratings for movies based on a sparse matrix of existing user-movie interactions. The technique of SVD allows us to decompose the matrix and reconstruct it with an approximation that helps in predicting missing ratings.

## Project Structure

- **Data Preparation**: The dataset used in this project is the 'ratings_small.csv' file, which contains user ratings for different movies. This file is part of the larger "Movies Dataset" available on Kaggle.
  
- **Matrix Factorization**: The core of this project involves applying SVD to the user-movie rating matrix to predict missing values. SVD allows us to reduce the dimensionality of the data while capturing important latent features of users and movies.

## Steps

1. **Data Extraction**: The zip file containing the dataset is extracted into a folder, and the CSV data is loaded into a Pandas DataFrame.
2. **Matrix Creation**: We create a pivot table of users and movie ratings to form the user-movie interaction matrix.
3. **Matrix Decomposition**: Using SVD, we decompose the rating matrix into three matrices: U, Sigma, and V^T. We retain only the largest singular values to approximate the matrix, ignoring smaller ones to reduce noise.
4. **Prediction**: The system randomly selects entries in the matrix, corrupts the value, and attempts to predict it based on the approximation generated from SVD.
5. **Error Calculation**: The prediction error (difference between the original value and the predicted value) is calculated and visualized using a histogram.

## Running the Project

1. Download the dataset from Kaggle: `!kaggle datasets download -d rounakbanik/the-movies-dataset`.
2. Extract the dataset by running the code.
3. Run the script to load the data, create the rating matrix, and predict missing ratings.
4. Visualize the prediction errors in the form of a histogram.

## Requirements

- Python 3.x
- NumPy
- Pandas
- Matplotlib
- SciPy

You can install the necessary packages using:

```bash
pip install numpy pandas matplotlib scipy
