## 📘 What is an API?
API (Application Programming Interface) is a set of rules that allows two software systems to communicate. Think of it like a restaurant menu — the menu lists dishes (API endpoints), you place an order (request), and the kitchen (server) prepares and delivers it (response).

---

## 🧩 Why APIs Are Important
APIs enable software systems to connect and share data. Examples include:
- Weather apps using OpenWeather API.
- YouTube using YouTube Data API.
- Google Maps providing directions via Maps API.
- Payment apps like PayPal using APIs for transactions.

---

## ⚙️ How APIs Work
1. The **Client** sends a **Request** to the **Server**.
2. The **Server** processes and sends a **Response** back.

Example:
```
Request: GET https://api.github.com/users/octocat
Response: { "login": "octocat", "followers": 3200, "repos": 8 }
```

---

## 📚 Key Terminology

| Term | Description | Example |
|------|--------------|----------|
| **Endpoint** | The URL path to access a resource | `/users`, `/posts`, `/weather?q=Delhi` |
| **Request** | What you send (GET, POST, PUT, DELETE) | `GET /users` |
| **Response** | What you receive from the API | JSON, XML, HTML |
| **Status Code** | Server response status | `200 OK`, `404 Not Found`, `500 Error` |
| **Headers** | Metadata about request/response | Content-Type, Authorization |
| **Authentication** | Security mechanism to access private APIs | API Key, OAuth Token |

---

## 🧱 Types of APIs

### 1️⃣ Based on Access and Use
| Type | Description | Example |
|------|--------------|----------|
| **Open/Public API** | Anyone can use, usually with a key | OpenWeather, NewsAPI |
| **Private API** | Used internally | HR systems |
| **Partner API** | Shared between companies | Amazon Partner API |
| **Composite API** | Combines multiple APIs | Dashboard APIs |

### 2️⃣ Based on Architecture
#### 🔹 REST API (Most Common)
Uses HTTP methods (GET, POST, PUT, DELETE), returns JSON, and is stateless.

#### 🔹 SOAP API
Uses XML and strict structure. Common in enterprise and finance.

#### 🔹 GraphQL API
Single endpoint, flexible queries. Used by Facebook, GitHub.

#### 🔹 WebSocket API
Two-way communication, used in chats, stock tickers, real-time apps.

#### 🔹 gRPC API
Binary-based, uses Protocol Buffers, and is fast and used in microservices.

---

## 🔑 HTTP Methods

| Method | Description | Example |
|---------|--------------|----------|
| **GET** | Retrieve data | `/users` |
| **POST** | Create data | `/users` |
| **PUT** | Update entire record | `/users/5` |
| **PATCH** | Update partial record | `/users/5` |
| **DELETE** | Remove record | `/users/5` |

---

## 📦 Data Formats

| Format | Description | Example |
|---------|--------------|----------|
| JSON | Human-readable, common | `{ "name": "Teju" }` |
| XML | Structured, older systems | `<user><name>Teju</name></user>` |
| YAML | Config format | `name: Teju` |
| CSV | Tabular format | `id,name\n1,Teju` |

---

## 🧰 Using APIs in Python

### Install Requests
```
pip install requests
```

### GET Example
```python
import requests
url = "https://api.github.com/users/octocat"
response = requests.get(url)
print(response.status_code)
print(response.json())
```

### POST Example
```python
import requests
url = "https://jsonplaceholder.typicode.com/posts"
payload = {"title": "API Demo", "body": "Learning APIs", "userId": 1}
response = requests.post(url, json=payload)
print(response.json())
```

### Using Headers & Keys
```python
import requests
url = "https://api.openweathermap.org/data/2.5/weather"
params = {"q": "Hyderabad", "appid": "YOUR_API_KEY", "units": "metric"}
response = requests.get(url, params=params)
print(response.json())
```

---

## 📊 HTTP Status Codes

| Code | Meaning | Description |
|-------|----------|-------------|
| 200 | OK | Request successful |
| 201 | Created | Resource created |
| 400 | Bad Request | Invalid input |
| 401 | Unauthorized | Invalid API key |
| 404 | Not Found | Resource missing |
| 500 | Server Error | Internal issue |

---




