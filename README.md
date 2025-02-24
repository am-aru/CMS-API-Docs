# CMS-API-Docs
## 📜 Content Management API Documentation
### Version: 1.0  
### Author: Arpita Sharma  
### Last Updated: 24 Feb 2025  
### GitHub Repository: CMS-API-Docs  
 

---

### Introduction  
The **Content Management API** allows developers to manage **blog posts** through a **RESTful API** built with **JavaScript (Node.js & Express)**. This API supports **CRUD operations** (Create, Read, Update, Delete) and integrates easily with front-end applications using **JavaScript & CSS**.

---

### Base URL  
https://api.example.com/v1

📌 **Note:** Replace `api.example.com` with the actual deployed API URL.

---

### Authentication & Headers  
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
    "author": "Arpita",
    "published_at": "2024-02-01"
  }
]
```
2️⃣ Create a New Blog Post (Requires API Key)
	•	Endpoint: POST /posts
	•	Headers Required:
 ```
{
  "Authorization": "Bearer <YOUR_API_KEY>"
}
```
• Request Body (JSON):
```
{
  "title": "How to Use JavaScript Fetch API",
  "content": "The Fetch API in JavaScript is used to make HTTP requests...",
  "author": "Alice Johnson"
}
```
3️⃣ Update a Blog Post (Requires API Key)
	•	Endpoint: PUT /posts/{postId}
	•	Headers Required:
 ```
{
  "Authorization": "Bearer <YOUR_API_KEY>"
}
```
4️⃣ Delete a Blog Post (Requires API Key)
	•	Endpoint: DELETE /posts/{postId}
	•	Response Example (Success - 200):
 ```
{
  "message": "Post deleted successfully"
}
```
📌 How to Use This API with JavaScript

Developers can fetch posts and display them in the frontend using JavaScript Fetch API.
```
fetch("https://api.example.com/v1/posts")
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.log("Error fetching posts:", error));
```
📌 Error Handling  

| **Error Code** | **Message**     | **Description**                             |
|--------------|---------------|-----------------------------------------|
| **400**     | `Bad Request`  | Missing required fields.               |
| **401**     | `Unauthorized` | Invalid API key.                       |
| **403**     | `Forbidden`    | API key missing or expired.            |
| **404**     | `Not Found`    | Requested blog post doesn’t exist.     |



	

