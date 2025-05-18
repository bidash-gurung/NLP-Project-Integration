# 🔗 Model Integration – Flask API for Hate Speech Detection

To bridge the AI model and the Chrome Extension, we developed a lightweight **Flask API** that exposes the trained GRU and LSTM models for real-time hate speech prediction.

---

## ⚙️ Integration Overview

The backend server is built using **Flask**, a Python web framework, to:

- Serve the trained NLP model
- Accept POST requests with text content
- Return prediction results to the Chrome Extension in JSON format

---

## 🧩 System Architecture

Chrome Extension
↓ (sends text)
[JavaScript fetch()]
↓
Flask API (Python)
↓
GRU / LSTM Model
↓
Response (Hate/Not Hate)
↓
Extension UI Displays Result


---

## 🧪 Sample API Usage

**Endpoint:** `POST /predict`

**Request Body (JSON):**
```json
{
  "text": "Example comment to analyze"
}

{
  "prediction": "hate_speech"
}
