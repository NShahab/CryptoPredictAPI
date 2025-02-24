# CryptoPredictAPI

CryptoPredictAPI is a Flask-based REST API that fetches real-time cryptocurrency data from Binance, applies technical indicators, and predicts future prices using an LSTM deep learning model.

## Features
- Fetches real-time OHLCV (Open, High, Low, Close, Volume) data from Binance API.
- Computes technical indicators such as SMA, RSI, and Bollinger Bands.
- Uses a trained LSTM model to predict future cryptocurrency prices.
- Provides a RESTful API endpoint for easy integration.

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
```sh
python app.py
```
The API will start on `http://127.0.0.1:5000/`

### API Endpoint
#### **GET /predict_price**
Fetches real-time data and predicts the price.

**Request Example:**
```
GET /predict_price?symbol=BTCUSDT&interval=4h
```

**Response Example:**
```json
{
  "symbol": "BTCUSDT",
  "interval": "4h",
  "predicted_price": 45000.25
}
```

## Deployment
To deploy on **Render**, **Heroku**, or any cloud service, follow these steps:

### Deploy on Render
1. Push your project to GitHub.
2. Create a **new service** on [Render](https://render.com/).
3. Connect your GitHub repository and select an environment (e.g., Flask).
4. Set the **start command** to:
   ```sh
   gunicorn app:app
   ```
5. Deploy and get your live API URL!

## Model Training
If you want to train your own LSTM model, ensure you have historical cryptocurrency data and use TensorFlow/Keras for training. You can replace `best_model.keras` with your trained model.

## Contributing
Pull requests are welcome! Feel free to submit improvements or report issues.

## License
This project is licensed under the MIT License.


