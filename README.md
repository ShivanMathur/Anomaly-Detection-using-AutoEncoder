# Anomaly-Detection-using-AutoEncoder

The project's objective is to utilize the AutoEncoder architecture to detect anomalies in the real production traffic data so that the organization can take appropriate action whenever they encounter such scenarios. 

## Dataset Description:

- The dataset has been taken from Yahoo Webscope program. It consists of time-series data with labeled anomalies. The data represents real production traffic of some Yahoo properties. The dataset comprises of three columns, namely:
  • timestamp: in the dataset, it is replaced by integers incremented by 1, which represents 1 hour worth of data.;
  • value: value recorded at the corresponding timestamp.; and
  • is_anomaly: Boolean indicating if the current value at the given timestamp is an anomaly or not.
- Dataset link: https://webscope.sandbox.yahoo.com/catalog.php?datatype=s&did=70

## Implementation:

- **Data Preprocessing:** 

- **Model Architecture:** 

- **Training and Evaluating the VGG-13 Model:**
  - **Training Process:** 

  - **Validation and Testing:**  

- **Model Evaluation:** 


## Model Performance:
- Basic Model: Initially developed the model without optimization techniques, serving as a baseline for further improvements.

- Optimization Techniques:

  - Regularization: Introduced L2 regularization by adding a weight decay parameter of 1e-5 to the optimizer. This technique helps prevent overfitting by penalizing large weights, which improved model generalization and increased accuracy to 92.00%.

  - Dropout: Added dropout layers with a probability of 0.5 between the fully connected layers to reduce overfitting by randomly dropping neurons during training. Although this technique slightly decreased test accuracy to 90.84%, it enhanced model robustness.

  - Early Stopping: Implemented early stopping to monitor validation loss and halt training if improvement ceased for a specified number of epochs (patience value of 4). The training concluded at epoch 19, with saved model weights showing a training accuracy of 92.71% and loss of 0.0018, and validation accuracy of 94.167% and loss of 0.0019. This approach significantly increased test accuracy to 93.02% and reduced test loss to 0.1995.

  - Image Augmentation: Applied image augmentation techniques including resizing images to 64x64 pixels and random horizontal flipping with a probability of 0.5. Despite these alterations, test accuracy was 87.46% with a loss of 0.3422, indicating the impact of dataset variation on model performance.


### Code:

The complete project code is available in the <a href = "https://github.com/ShivanMathur/VGG-Image-Classification/blob/main/VGG_Image_Classification.ipynb"> VGG_Image_Classification.ipynb</a>.

### Report:

For a detailed project report, <a href = "https://github.com/ShivanMathur/VGG-Image-Classification/blob/main/report.pdf" > click here</a>.

### Contact:
For questions or feedback, please reach out to me at [shivanmthr18@gmail.com](mailto:shivanmthr18@gmail.com).
