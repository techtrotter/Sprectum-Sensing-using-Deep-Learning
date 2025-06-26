# 📡 Spectrum Sensing using Deep Learning

This project demonstrates the use of deep learning for automatic modulation classification in wireless communication systems. It applies a Convolutional Neural Network (CNN) to identify signal modulation types across varying levels of noise, supporting robust spectrum sensing for cognitive radio networks.

---

## 🧠 Methodology

### 📦 Dataset
- Used **RadioML 2016.04C** dataset containing 2×128 complex I/Q signal samples.
- Modulations include: BPSK, QPSK, AM-DSB, FM, QAM16, QAM64, GFSK, etc.
- SNR levels range from **-20 dB to +20 dB**.

### 🧱 Model Architecture
- Input Reshaping: Converts `[2, 128]` to `[2, 128, 1]`.
- Convolutional Layers: Stacked Conv2D + MaxPooling + ReLU activations.
- Regularization: Dropout + L2 penalty.
- Classifier: Flatten → Dense → Softmax.
- Loss: Categorical Cross-Entropy, Optimizer: Adam

---

## 📊 Results

### 📈 Accuracy vs. SNR

| SNR (dB) | Accuracy (%) |
|----------|---------------|
| -20      | 22.3%         |
| -10      | 46.5%         |
| 0        | 64.9%         |
| 10       | 88.7%         |
| 20       | 96.3%         |

### 🔍 Confusion Matrix Highlights
- **At -20 dB**: Misclassification common between QAM16/QAM64 and AM/FM.
- **At ≥10 dB**: Excellent separation with >90% classification accuracy.

---

## ✅ Conclusion

The CNN architecture effectively classifies modulation types even under high noise levels, enabling intelligent spectrum utilization in cognitive radio systems.

### 📈 Potential Improvements:
- Integration with SDR tools (e.g., GNU Radio)
- Adversarial robustness and real-time streaming
- Transfer learning for dynamic wireless environments

---

## 📁 Project Assets
- `project_code.ipynb` — Model training & evaluation
- `model_d1.wts.h5` to `model_d4.wts.h5` — Trained weights
- `2016.04C.multisnr.pkl` — Dataset (not included due to size)

To request dataset or collaborate:
📧 **blb8.dev@gmail.com**

---

## 👨‍💻 Author

**Bijoy Laxmi Biswas**  
Engineer | Techie Traveler | Deep Learning Enthusiast  
🔗 [LinkedIn](https://www.linkedin.com/in/bijoy-laxmi-biswas-cse07/)
