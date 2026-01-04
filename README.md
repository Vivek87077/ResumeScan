# 🚀 Resume Analyzer

[![Live App](https://img.shields.io/badge/Live-App-brightgreen)](https://resume-analyser-kp0f.onrender.com/)


## 📌 Description

**Resume Analyzer** is a full-stack web application that uses **Artificial Intelligence** to analyze resumes and provide meaningful insights such as:

- Skill extraction  
- Resume quality evaluation  
- Improvement suggestions  

The project integrates **Google Gemini AI** for intelligent resume analysis and implements secure authentication features including **email verification** and **password reset** using **Brevo**.

---

## 🛠️ Tech Stack

| Layer | Technology |
|-----|-----------|
| Frontend | HTML, CSS, React.js |
| Backend | Spring Boot |
| Database | MySQL |
| AI Engine | Google Gemini AI |
| Email Service | Brevo |

---

## 👀 Preview

<p align="center">
  <img width="30%" src="https://github.com/user-attachments/assets/df7bb0c1-1f10-478d-b8c9-c2b1bf2369f4" />
  <img width="30%" src="https://github.com/user-attachments/assets/1c65a0cc-c915-4103-a7fe-30a975639ab0" />
  <img width="30%" src="https://github.com/user-attachments/assets/b8ca21ad-7c2f-470d-ad5d-73119b8fd9f1" />
</p>

<p align="center">
  <img width="30%" src="https://github.com/user-attachments/assets/3f945bf1-84dd-4052-9c65-709f512ae0a4" />
  <img width="30%" src="https://github.com/user-attachments/assets/d04af8b7-4e12-4948-94c6-3b1f15340180" />
  <img width="30%" src="https://github.com/user-attachments/assets/a0c6f513-2108-41c8-98b5-91e86d27d398" />
</p>

---

## 🔗 Frontend & Backend Integration

- Frontend UI is developed using **React.js**
- For deployment, the React app is **built and served by Spring Boot**
- React production build files are placed inside the backend **`static` directory**

### 📁 Static & Template Files

- `static/`  
  - Contains React **production build files**
- `templates/` (inside static)  
  - Stores email templates for:
    - Email verification
    - Password reset

---

## ▶️ How to Run the Project Locally

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/Mohamed-Imran-12/Resume-Analyser.git
```

### 2️⃣ Open Project in IDE
- Open in IntelliJ IDEA or Eclipse
- Open pom.xml and allow Maven to download dependencies

### 3️⃣ Configure Credentials (application.properties)
🗄️ Database (MySQL ONLY)
```bash
spring.datasource.url=your_DB_URL
spring.datasource.username=your_DB_USERNAME
spring.datasource.password=your_DB_PASSWORD
```

🔐 Google Cloud Platform (Google Sign-In)
```bash
spring.security.oauth2.client.registration.google.client-id=your_GCP_ID
spring.security.oauth2.client.registration.google.client-secret=your_GCP_SECRET
```

🤖 Google Gemini AI (Resume Analysis)
```bash
genKey=your_GEMINI_API_KEY
```

📧 Mail Service (Brevo ONLY)
```bash
apiKey=your_BREVO_MAIL_API
```

### 4️⃣ Run Backend
Run:
```bash
ResumeAnalyserApplication.java
```

### 5️⃣ Open in Browser
```bash
http://localhost:8080/
```

<hr>

## ⚠️ Important Notes (Must Read)
- Only Google Gemini AI is configured
  ➜ To use another AI provider, update AI-related logic in ``` appservice.java ```

- Email functionality works only with Brevo API
  ➜ To change mail provider, update ``` mailservice.java ```

- AI models evolve rapidly
  ➜ If the configured Gemini model is deprecated, update it in ``` appservice.java ```

<hr>

## 🎨 Modifying the Frontend UI
🚫 Do NOT edit files inside backend static directory directly <br>
🔧 Development Mode (Frontend Only)
```bash
cd "frontend src"
npm install
npm run dev
```
This runs the React development server for UI changes.

📦 Build Frontend for Backend Deployment
```bash
cd "frontend src"
npm run build
```

📂 Backend Static Structure
```text
static/
├── assets/
│   ├── *.css
│   ├── *.js
├── index.html
```

✔️ Deployment Steps

1. Delete old index.html and files inside assets
2. Copy new build files from dist
3. Paste them into backend static directory

<hr>

### Author : ``` Vievk Sharma ```
