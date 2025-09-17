
# Weather Prediction using RNN

## Project Overview

This project aims to predict weather parameters for the next day based on historical weather data using a Recurrent Neural Network (RNN). The system takes past sequences of weather features and outputs a predicted value for the following day. It is implemented in Python with libraries such as NumPy and PyTorch.

---

## Process

### 1. Data Collection and Preprocessing

* Collected historical weather data consisting of multiple parameters (e.g., temperature, humidity, wind speed, pressure) over a period of time.
* Each day is represented as a vector of features.
* Normalized the dataset to scale the features between 0 and 1 for efficient training of the RNN.
* Prepared sequences of a fixed length (e.g., 7 days) as input and the next day’s values as targets.
* Split the dataset into training and testing sets to evaluate model performance.

### 2. Model Training

* Defined the RNN model using PyTorch.
* Input: sequence of past weather data (sequence length × number of features).
* Output: predicted weather values for the next day.
* Loss function: Mean Squared Error (MSE) between predicted and actual values.
* Optimizer: Adam optimizer to minimize the loss.
* Trained the model over multiple epochs, monitoring the loss on both training and validation sets.
* Saved the trained model for inference.

### 3. Prediction

* Used the trained model to predict weather for the next day given a new sequence.
* Implemented denormalization to convert predictions back to original scale.
* Evaluated predictions against the ground truth using metrics such as MSE and visual plots.


---

## Model Architecture

The RNN model consists of:

1. **Input Layer**: Accepts sequences of past weather features.
2. **Recurrent Layer (RNN)**:

   * Processes sequential data and maintains temporal dependencies.
   * Captures patterns in weather variations over time.
3. **Fully Connected Layer (Dense Layer)**:

   * Maps the RNN output to the predicted weather parameters for the next day.
4. **Output Layer**: Produces the final predicted weather vector.

**Optional Improvements:**

* Use **LSTM or GRU** for better handling of long-term dependencies.
* Add **dropout** layers to prevent overfitting.
* Experiment with **different sequence lengths** and hidden units to optimize accuracy.

---

## Results

* The model successfully predicts the next day’s weather parameters given the previous sequence.
* Sample metrics on test data:

  * **Mean Squared Error (MSE)**: \[Provide value based on your training]
  * **Mean Absolute Error (MAE)**: \[Provide value based on your training]
* Sample predictions compared to actual values show that the model captures trends in temperature, humidity, and other features.

**Limitations:**

* Prediction accuracy may drop for highly volatile weather conditions.
* The simple RNN model has limitations in capturing long-term dependencies compared to LSTM/GRU models.

---




