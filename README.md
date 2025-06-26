 Spectrum Sensing using Deep Learning
Author: techtrotter
Project: Sprectum-Sensing-using-Deep-Learning

 Overview
This project applies deep learning techniques for automatic modulation classification — a key problem in cognitive radio systems. Using a convolutional neural network (CNN), we train models to classify various modulation types across multiple Signal-to-Noise Ratios (SNRs), enabling smarter spectrum utilization.

 What’s Inside
✅ Dataset: 2016.04C.multisnr.pkl (RadioML)

✅ Modulation types across different SNRs

✅ CNN-based architecture using Keras/TensorFlow

✅ Confusion matrix visualization

✅ Trained model weights:

model_d1.wts.h5

model_d2.wts.h5

model_d3.wts.h5

model_d4.wts.h5

 Dataset
RadioML 2016.04C dataset is used, containing modulation types such as:

QAM16, QAM64

BPSK, QPSK

AM, FM

And more...

Signals are structured with corresponding SNR levels.

Model Architecture
The model uses:

Convolutional layers for feature extraction

Gaussian noise layers to simulate signal variation

Dense layers for final classification

📁 Project Structure
bash
Copy
Edit
.
├── project_code.ipynb         # Main Jupyter notebook
├── model_d1.wts.h5            # Trained model weights (1 of 4)
├── model_d2.wts.h5
├── model_d3.wts.h5
├── model_d4.wts.h5
└── README.md                  # This file
🛠️ How to Run
Clone the repository:

bash
Copy
Edit
git clone https://github.com/techtrotter/Sprectum-Sensing-using-Deep-Learning.git
cd Sprectum-Sensing-using-Deep-Learning
Install dependencies:
bash
Copy
Edit
pip install -r requirements.txt
Run the notebook:

Open project_code.ipynb in Jupyter

Follow the cells to train or load models and evaluate performance

📈 Results
High classification accuracy at moderate to high SNR levels

Confusion matrices provide insight into model confidence

Performance drops gracefully in low SNR scenarios


****Future Work****
Try LSTM or hybrid models for temporal analysis

Deploy the model using Flask or Streamlit

Experiment with real-time spectrum sensing using SDRs

