# CMS-API-Docs
## 📜 Content Management API Documentation
### Version: 1.0  
### Author: Arpita Sharma  
### Last Updated: 24 Feb 2025  
### GitHub Repository: CMS-API-Docs  
 

---

## 📌 Introduction  
The **Content Management API** allows developers to manage **blog posts** through a **RESTful API** built with **JavaScript (Node.js & Express)**. This API supports **CRUD operations** (Create, Read, Update, Delete) and integrates easily with front-end applications using **JavaScript & CSS**.

---

### 📌 Base URL  
https://api.example.com/v1

📌 **Note:** Replace `api.example.com` with the actual deployed API URL.

---

### 📌 Authentication & Headers  
- **Public endpoints (GET requests) do not require authentication.**  
- **POST, PUT, DELETE requests require an API Key** in the header.  

📌 **Headers Example (Authenticated Requests)**  
```json
{
  "Authorization": "Bearer <YOUR_API_KEY>",
  "Content-Type": "application/json"
}
```
📌 API Endpoints

1️⃣ Fetch All Blog Posts (Public)
	•	Endpoint: GET /posts
	•	Response Example (Success - 200):
```
[
  {
    "id": 1,
    "title": "Introduction to JavaScript",
    "content": "JavaScript is a powerful scripting language...",
    "author": "John Doe",
    "published_at": "2024-02-01"
  }
]
```
