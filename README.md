📈 Microsoft Stock Price Prediction using LSTM 📝 Project Overview This project implements a time series forecasting model to predict Microsoft’s stock closing price using historical data and a deep learning LSTM model. It analyses past stock behaviour to forecast future prices, demonstrating practical applications of deep learning in financial data analysis.

💡 Problem Statement Predict the future closing price of Microsoft stocks based on its historical Open, High, Low, Close, and Volume data. This helps traders, analysts, and learners understand LSTM (Long Short-Term Memory) networks for sequential data and market trend forecasting.

📂 Dataset Used Source: Kaggle dataset – downloaded directly in Google Colab
Dataset: Microsoft Stock Price historical data
Features: Date, Open, High, Low, Close, Volume
Target: Close price

🔧 Installation & Requirements Open the notebook in Google Colab.
Mount Google Drive (if saving outputs) and install dependencies:
python Copy Edit !pip install tensorflow pandas numpy matplotlib seaborn scikit-learn kaggle Download dataset from Kaggle within Colab:
python Copy Edit from google.colab import files files.upload() # upload your kaggle.json
!mkdir -p ~/.kaggle !cp kaggle.json ~/.kaggle/ !chmod 600 ~/.kaggle/kaggle.json
!kaggle datasets download <dataset-identifier> !unzip <downloaded-file.zip> (Replace <dataset-identifier> with your actual dataset path on Kaggle)

🚀 How to Run Run the stock_pred.ipynb notebook step by step in Google Colab.
The notebook will:
Install necessary libraries
Authenticate and download data from Kaggle
Load and preprocess the dataset
Visualize data trends and insights
Build and train an LSTM model
Predict and plot actual vs predicted stock closing prices

📊 Project Structure Copy Edit stock-price-prediction/ ├── stock_pred.ipynb └── README.md (Data is downloaded dynamically from Kaggle, hence no CSV stored here.)
🔍 Results ✅ Model:
Two LSTM layers (64 units each)
Dense layer (128 units, ReLU activation)
Dropout layer (0.5) to prevent overfitting
Output Dense layer (1 unit, linear activation)

✅ Training:
Optimizer: Adam
Loss: MAE
Epochs: 20
Batch Size: 32

✅ Evaluation:
Predictions plotted against actual stock closing prices.

📈 Sample Output Visualization (Add your final plotted graph here after saving it in Colab for GitHub upload)

python Copy Edit plt.figure(figsize=(14,6)) plt.plot(test['date'], test['close'], label='Actual Close Price') plt.plot(test['date'], test['prediction'], label='Predicted Close Price') plt.xlabel('Date') plt.ylabel('Close Price') plt.title('Microsoft Stock Price Prediction') plt.legend() plt.show() 💭 Future Improvements Tune hyperparameters (number of units, layers, dropout rates) for enhanced performance
Use Bidirectional LSTM for capturing trends in both directions
Incorporate market sentiment or news headlines as features
Deploy as an interactive Streamlit or Flask web app for real-time predictions

🙌 Acknowledgements Dataset from Kaggle Microsoft Stock Price Data

Built for practicing Deep Learning for Time Series Forecasting concepts

✨ Author Sanskar Pandey B.Tech CSE | Aspiring Data Scientist

LinkedIn • GitHub • Email
