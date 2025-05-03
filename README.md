# LSTM-Based Time Series Forecasting

This project showcases the application of Long Short-Term Memory (LSTM) neural networks for univariate time series forecasting using Keras and TensorFlow. LSTMs are a type of recurrent neural network (RNN) well-suited to modeling temporal sequences and long-range dependencies.

## Objective

To build an LSTM model capable of predicting future values in a time series dataset by learning from historical data patterns.

## Project Workflow

1. **Data Preprocessing**
   - Loaded and visualized the time series data using Pandas and Matplotlib.
   - Normalized the dataset to a [0,1] scale using MinMaxScaler for optimal LSTM performance.
   - Generated input-output pairs using sliding windows to create sequences of past values.

2. **Model Architecture**
   - Constructed a Sequential model using:
     - 1 LSTM layer with 50 units
     - 1 Dense output layer
   - Configured with `mean_squared_error` loss and the `adam` optimizer.

3. **Training**
   - Trained the model for 100 epochs with a batch size of 32.
   - Split the dataset into training and test sets (typically 80/20).
   - Evaluated the model using Root Mean Squared Error (RMSE).

4. **Prediction and Visualization**
   - Predicted future values from test input.
   - Inverse-transformed predictions back to original scale.
   - Plotted predicted vs. actual values to visualize forecasting accuracy.

## Results

- Achieved an RMSE of **[0.045]** on test data.
- The LSTM model successfully captured seasonality and short-term trends in the dataset.
- Clear visual alignment of prediction and actual values demonstrated model effectiveness.

## Technologies Used

- **Python 3.8**
- **Libraries:** NumPy, Pandas, Matplotlib, Scikit-learn, TensorFlow, Keras

