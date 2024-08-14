# Anomaly-Detection-using-AutoEncoder

The project's objective is to utilize the AutoEncoder architecture to detect anomalies in the real production traffic data so that the organization can take appropriate action whenever they encounter such scenarios. 

## Dataset Description:

- The dataset has been taken from Yahoo Webscope program. It consists of time-series data with labeled anomalies. The data represents real production traffic of some Yahoo properties. The dataset comprises of three columns, namely:
  • timestamp: in the dataset, it is replaced by integers incremented by 1, which represents 1 hour worth of data.;
  • value: value recorded at the corresponding timestamp.; and
  • is_anomaly: Boolean indicating if the current value at the given timestamp is an anomaly or not.
- Dataset Link: <a href = "https://webscope.sandbox.yahoo.com/catalog.php?datatype=s&did=70"> Yahoo Webscope S5 Dataset</a>

## Implementation:

- **Data Preprocessing:**
  - Imported and combined multiple CSV files containing time series data from the A1Benchmark dataset. The dataset was merged into a single DataFrame for easier manipulation and analysis.
  - Verified the dataset for any missing values to ensure data quality and consistency before proceeding with further steps.
  - Performed normalization on the dataset using the StandardScaler from Scikit-learn. This scaling ensures that the features have a mean of 0 and a standard deviation of 1. 

- **Model Architecture:**

  - Model 1: Dense AutoEncoder

    - This model is a straightforward autoencoder built with fully connected (dense) layers. It includes three encoding layers and three corresponding decoding layers. The model is designed to compress the input data into a smaller latent representation and then reconstruct the original data.

  - Model 2: LSTM-based AutoEncoder

    -  This model utilizes LSTM layers for both the encoder and decoder. It is designed to capture temporal dependencies in sequential data, making it well-suited for time series anomaly detection.

  - Model 3 & 4: Enhanced AutoEncoder with Modified Hyperparameters
    - An extension of Model 1, this version replaces ReLU with Tanh activation functions and increases the hidden units. The adjustments in activation functions and hidden layer dimensions aim to improve the model's learning capabilities. 
   
   - Building on Model 3, this architecture replaces Tanh with LeakyReLU activation functions and introduces Dropout layers for regularization. These changes help prevent overfitting and enhance the model's robustness. 

## Model Performance:
- Model 2 with LSTM architecture achieves the highest accuracy (93.93%), followed by Model 3 (93.63%), Model 1 (93.438%) and then Model 4 (93.05%).
- Model 2 has the highest precision and recall, which indicates that it can correctly identify and capture anomalies. It also shows the highest number of true positives and lowest number of false negatives.


### Code:

The complete project code is available in the <a href = "https://github.com/ShivanMathur/Anomaly-Detection-using-AutoEncoder/blob/main/Anomaly_Detection_using_AutoEncoder.ipynb"> Anomaly_Detection_using_AutoEncoder.ipynb </a>.

### Report:

For a detailed project report, <a href = "https://github.com/ShivanMathur/Anomaly-Detection-using-AutoEncoder/blob/main/report.pdf" > click here</a>.

### Contact:
For questions or feedback, please reach out to me at [shivanmthr18@gmail.com](mailto:shivanmthr18@gmail.com).
