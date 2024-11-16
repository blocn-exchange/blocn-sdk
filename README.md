# BLOCN Exchange SDK

<p align="center">
  <img src="https://github.com/user-attachments/assets/92907e60-c0a9-4e44-b651-b489cb660257" alt="BLOCN SDK" width="200"/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/python-v3.7+-blue.svg" alt="Python">
  <img src="https://img.shields.io/badge/nodejs-v14+-green.svg" alt="Node.js">
  <img src="https://img.shields.io/badge/java-v11+-red.svg" alt="Java">
  <img src="https://img.shields.io/badge/go-v1.16+-blue.svg" alt="Go">
  <img src="https://img.shields.io/badge/license-MIT-blue.svg" alt="License">
</p>

## 📦 Supported Languages

- [Python SDK](./python)
- [JavaScript SDK](./javascript)
- [Java SDK](./java)
- [Go SDK](./golang)

## 🚀 Quick Start

### Python Installation

bash
pip install blocn-sdk


### Python Example

python
from blocn_sdk import Client

# Initialize the client
client = Client(api_key='your_api_key', api_secret='your_api_secret')

# Get account balance
balance = client.get_account_balance()
print(balance)

# Place a market order
order = client.create_order(
    symbol='BTC-USDT',
    side='BUY',
    type='MARKET',
    quantity=0.01
)


### JavaScript Installation

bash
npm install blocn-sdk


### JavaScript Example

javascript
const { Client } = require('blocn-sdk');

// Initialize the client
const client = new Client({
    apiKey: 'your_api_key',
    apiSecret: 'your_api_secret'
});

// Get market ticker
client.getTicker('BTC-USDT')
    .then(ticker => console.log(ticker))
    .catch(error => console.error(error));


## 📚 Features

- ✅ Complete API Coverage
- 🔒 Secure Authentication
- ⚡ WebSocket Support
- 📈 Real-time Market Data
- 💼 Order Management
- 🔄 Automatic Rate Limiting
- 🛡️ Error Handling
- 📊 Data Normalization

## 📖 Documentation

Detailed documentation for each language SDK:

- [Python Documentation](./python/README.md)
- [JavaScript Documentation](./javascript/README.md)
- [Java Documentation](./java/README.md)
- [Go Documentation](./golang/README.md)

## 💻 SDK Examples

### Market Data

python
# Python example
# Get market depth
depth = client.get_order_book('BTC-USDT', limit=20)

# Get recent trades
trades = client.get_recent_trades('BTC-USDT', limit=50)

# Get kline/candlestick data
klines = client.get_klines('BTC-USDT', interval='1h', limit=100)


### Trading Operations

python
# Place limit order
order = client.create_order(
    symbol='BTC-USDT',
    side='BUY',
    type='LIMIT',
    price=50000.00,
    quantity=0.01
)

# Cancel order
result = client.cancel_order(
    symbol='BTC-USDT',
    orderId='123456789'
)

# Get order status
status = client.get_order_status(
    symbol='BTC-USDT',
    orderId='123456789'
)


## 🔧 Installation Requirements

### Python SDK
- Python 3.7 or higher
- requests
- websocket-client
- aiohttp (for async support)

### JavaScript SDK
- Node.js 14 or higher
- axios
- ws
- typescript (for type definitions)

### Java SDK
- Java 11 or higher
- OkHttp3
- Jackson
- Lombok

### Go SDK
- Go 1.16 or higher
- gorilla/websocket
- go-resty

## 🤝 Contributing

We welcome contributions! Please see our [Contributing Guidelines](CONTRIBUTING.md) for details.

### Development Setup

bash
# Clone the repository
git clone https://github.com/blocn-exchange/blocn-sdk.git
cd blocn-sdk

# Install development dependencies
pip install -r requirements-dev.txt


## 🔍 Testing

bash
# Run Python tests
python -m pytest tests/

# Run JavaScript tests
npm test

# Run Java tests
mvn test

# Run Go tests
go test ./...


## 📝 Error Handling

All SDKs implement standardized error handling:

python
try:
    result = client.create_order(...)
except BlocnAPIException as e:
    print(f"API Error: {e.error_code} - {e.error_message}")
except BlocnRequestException as e:
    print(f"Request Error: {e}")


## 🔐 Security

- All API requests are encrypted using TLS 1.2/1.3
- API credentials are never logged or exposed
- Automatic request signing
- Optional IP whitelist support

## 💬 Support

- 📧 SDK Support: sdk-support@blocn1.com
- 💭 Discord: [BLOCN Developers](https://discord.gg/blocn-dev)
- 📚 API Docs: [BLOCN API Documentation](https://github.com/blocn-exchange/blocn-api-docs)

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

<p align="center">
  <b>Build with BLOCN Exchange SDK</b>
</p>

<p align="center">
  <a href="https://www.blocn1.com">Website</a> •
  <a href="https://www.youtube.com/@Blocn_Official">Youtube</a> •
  <a href="https://x.com/blocn_global">Twitter</a> •
  <a href="https://blocn.medium.com/">Medium</a> •
  <a href="https://www.instagram.com/blocn_global/">Instagram</a>
</p>

<p align="center">
  © 2024 BLOCN Exchange. All Rights Reserved.
</p>
