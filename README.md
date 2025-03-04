# CryptoPredictAPI

CryptoPredictAPI is a Flask-based REST API that fetches real-time cryptocurrency data from Binance, applies technical indicators, and predicts future prices using an LSTM deep learning model.

---

## Features
- Fetches real-time OHLCV (Open, High, Low, Close, Volume) data from Binance API.
- Computes technical indicators such as SMA, RSI, and Bollinger Bands.
- Uses a trained LSTM model to predict future cryptocurrency prices.
- Provides a RESTful API endpoint for easy integration.

---

## Installation

### Prerequisites
Ensure you have the following installed:
- Python 3.8+
- pip (Python package manager)

### Clone the Repository
```sh
git clone https://github.com/yourusername/CryptoPredictAPI.git
cd CryptoPredictAPI
```

### Create a Virtual Environment (Optional but Recommended)
```sh
python -m venv venv
source venv/bin/activate   # On Windows: venv\Scripts\activate
```

### Install Dependencies
```sh
pip install -r requirements.txt
```

## Usage

### Start the API
Run the following command to start the API:
```sh
python app.py
```
The API will start on `http://127.0.0.1:5000/`.

## API Documentation

### GET /predict_price
Fetches real-time cryptocurrency data, computes technical indicators, and predicts the future price using the LSTM model.

**Parameters:**
- `symbol` (optional): The cryptocurrency trading pair (e.g., BTCUSDT). Default: BTCUSDT.
- `interval` (optional): The time interval for the data (e.g., 1h, 4h, 1d). Default: 4h.

**Example Request:**
```sh
GET /predict_price?symbol=BTCUSDT&interval=4h
```

**Example Response:**
```json
{
  "interval": "4h",
  "predicted_price": 98820.07316815377,
  "symbol": "BTCUSDT"
}
```

## Deployment

### Deploy on GitHub Codespaces
Open your repository in GitHub Codespaces.

Install dependencies:
```sh
pip install -r requirements.txt
```

Run the API:
```sh
python app.py
```
Access the API using the public URL provided by GitHub Codespaces (e.g., `https://your-codespace-url.app.github.dev/predict_price`).

## Model Training
If you want to train your own LSTM model, ensure you have historical cryptocurrency data and use TensorFlow/Keras for training. You can replace `models/model_LSTM_4h.keras` with your trained model.

## Contributing
Pull requests are welcome! Feel free to submit improvements or report issues.

## License
This project is licensed under the MIT License.
