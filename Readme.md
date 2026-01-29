# Real-Time Market Prediction System (LSTM)

An AI-powered system that connects to live financial markets, predicts price movements **10 seconds ahead**, and visualizes them on a dynamic real-time dashboard.

## 🚀 Features

*   **Real-Time Data Streaming**: High-frequency data ingestion using `yfinance`.
*   **LSTM Neural Network**: Time-series forecasting model built with TensorFlow/Keras.
*   **Predictive Dashboard**: Live Matplotlib visualization comparing Actual prices vs. Predicted future rates.
*   **Detailed Gridding**: Professional-grade chart visualization with major and minor grid lines for precise price tracking.
*   **Immediate Start**: Buffer pre-population allows the AI to start predicting the moment the script is launched.

---

## 🛠️ Installation

### 1. Requirements
*   Python 3.8+
*   TensorFlow
*   NumPy (< 2.0)
*   Pandas
*   Matplotlib
*   yfinance (Latest)
*   scikit-learn

### 2. Setup
Clone the repository and install dependencies:
```bash
pip install tensorflow "numpy<2" pandas matplotlib yfinance scikit-learn imutils
```

---

## 📈 Usage

### Run the Live Dashboard
Navigate to the `RealTimeMarket` directory and run the main entry point:
```bash
cd RealTimeMarket
python live_dashboard.py
```

*   **Blue Line**: Actual Market Price (BTC-USD).
*   **Orange Dashed Line**: Predicted Price (10-second forecast).
*   **Console Output**: Level-by-level numerical comparison of Actual vs. Predicted rates.

---

## 📂 Project Structure

```text
├── RealTimeMarket/
│   ├── data_stream.py      # Connection to yfinance API
│   ├── predictor.py        # LSTM Model architecture & inference logic
│   └── live_dashboard.py   # Main controller & Real-time visualization
├── artifacts/              # Dataset and training samples
├── config.py               # legacy configuration
└── README.md               # This documentation
```

---

## 🧠 Technical Overview

1.  **Data Processing**: The `DataStream` class fetches 1-minute interval data and simulates a high-frequency tick stream for the dashboard.
2.  **Modeling**: The `MarketPredictor` uses an LSTM (Long Short-Term Memory) network with Dropout layers to handle market noise and capture temporal dependencies.
3.  **Visualization**: Uses `matplotlib.animation` for a non-blocking interactive plot that updates every second.

---

## 📦 Archived System (Image-Based Chart Prediction)
The original system for predicting bounding boxes on static stock chart images is still available in the root directory:
*   `python evaluate.py`: Train and evaluate the image-based model.
*   `python predict.py -i <image_path>`: Predict on a specific chart image.

---
*Disclaimer: This tool is for educational purposes. Financial market prediction involves significant risk.*
