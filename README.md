The Wells Fargo and Company (WFC) data is selected from the data from January 1, 2007 to March 31, 2022. The data in one day denotes a point in the sequence.
The train set and test set were divided on July 16, 2021. This means that there are 3659 training samples and 180 testing samples

**AttCLX:** The AttCLX model is a hybrid, integrating various machine learning and deep learning techniques to predict stock prices.

**Description of the Model Architecture:**
    **Attention-based CNN (ACNN) as the Encoder:** Utilizes a self-attention layer and CNN to extract deep features and compute key components for the LSTM decoder.
    
    **Bidirectional LSTM as the Decoder:** Processes the input from the ACNN encoder, capturing long-term time series features and temporal dependencies.

**Purpose of Each Component:**
    CNN: Extracts deep features from the original stock data.
    LSTM: Mines long-term time series features.
    XGBoost: Fine-tunes the predictions for enhanced accuracy.


**Modification of model:**
1. The look back trick for time-series forecasting was adopted and the number is 20.
2. The layer number of LSTM is 5, and the size is 64. The epoch number is 50.
3. Model is trained by introducing dropout rate of 0.3. The head number is 4. The model is also trained through Adam optimizer and the learning rate is 0.01.

**CONCLUSION**
1. The stock market’s complex volatility makes price prediction challenging yet crucial for securing investor returns.
2. Traditional ARIMA models fall short in capturing nonlinearity in stock predictions.
3. The Hybrid model (AttCLX) significantly outperforms other models in all metrics: MAE, RMSE, MSE, and R².
4. AttCLX achieves an R² score of 0.97962, indicating a very high level of predictive accuracy.
