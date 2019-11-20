# Speed Challenge

Speed Challenge is a project I worked on to predict the speed of the car from frames of a dashcam video. Some technologies I used to accomplish this were Fast.ai, OpenCV, Matplotlib, NumPy, and Pandas. My basic approach was visualizing the speed and acceleration between each frame using optical flow and acceleration, and training the model based on that. In the end, my model had an MSE of 1.4 on the training set, but was clearly overfitting and performed poorly on the test set. Overall, I learned a lot about computer vision and the challenges associated with self driving cars through this project. 

# Data Preparation.ipynb

This notebook contains code to prepare my dataset. It contains augmentation functions to compute optical flow, crop, and resize images. It also contains code to prepare my training, valid, and test sets. 

# Model-Analysis.ipynb

This notebook contains code to analyze the performance of my model and optimize some parameters. The most notable part of this notebook is a function `get_weighted_avg` which optimizes the parameters for a weighted average between predictions. This turned out to greatly reduce noise in my predictions and improved performance greatly. This notebook also contains code to visualize my predictions and errors.

# Test-Analysis.ipynb

This notebook contains code to append my predictions for the test set onto the test set video so I could analyze where my model was making mistakes.

# Prediction.ipynb

This notebook makes predictions for my test set based on my trained model and a weighted average between predictions. The parameters for this weighted average were learned in `Model-Analysis.ipynb` 
