# CSV to JSON API Converter

Production-ready Flask API for converting CSV files to JSON via REST API.  
Includes rate-limiting, Docker, clean modular structure — всё для продакшена и продажи.

---

## 🚀 Features

- Upload any CSV and get instant JSON via API
- Works with large and multilingual CSV
- Rate limiting (anti-abuse, 5 uploads per minute)
- Docker-ready, clean project structure
- Simple API, easy integration (Postman, curl, любой front-end)
- Logging for audits and debugging

---

## 📦 Endpoints

### POST \`/convert/\`

**Request (form-data):**
- \`file\` (type: File) — upload your CSV

**Response:**
\`\`\`json
{
  "file_id": "uuid-here"
}
\`\`\`

---

### GET \`/convert/result/<file_id>\`

Returns parsed CSV as JSON.

**Response:**
\`\`\`json
[
  { "name": "Ali", "email": "ali@example.com" },
  { "name": "Ivan", "email": "ivan@example.com" }
]
\`\`\`

---

## ⏱️ Rate limits

- \`/convert/\`: 5 uploads per minute per IP
- \`/convert/result/<file_id>\`: 10 reads per minute per IP

---

## ⚡ Quick Start

### Docker (recommended)
\`\`\`bash
docker build -t csv-to-json-api .
docker run -d -p 5000:5000 csv-to-json-api
\`\`\`

### Local
\`\`\`bash
pip install -r requirements.txt
python app.py
\`\`\`

---

## 🖼️ Screenshots

- \`postman_upload_csv.png\` — Uploading CSV via Postman
- \`postman_get_json_result.png\` — Getting JSON result via file_id
- \`flask_server_log_success.png\` — Server log: conversion and result
- \`flask_server_startup.png\` — Flask API server startup

---

> 💡 See real examples on Gumroad or in this README.

---

## 💼 Ready-to-Use Version

You can get a ZIP version with all files, setup instructions, \`.env.example\`, and more:

👉 [Buy it on Gumroad](https://talabov.gumroad.com/)

---

## 📬 Contact

**Need this in another stack (Node.js, Go, etc)?**  
Contact: talabov.ali72@gmail.com  
Telegram: [@talabovali](https://t.me/talabovali)

*Note: Pricing may vary depending on complexity and target stack.*

---

**Ready for production and monetization. 100% tested.**
