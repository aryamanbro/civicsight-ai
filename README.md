# CivicSight AI

**CivicSight AI** is an AI-powered citizen issue reporting system. It allows users to capture and report civic issues using images or voice notes, which are then automatically classified and processed using machine learning models.

---

## 🏗️ Project Architecture

This project is built using a modern microservices-inspired architecture, consisting of three main components:

### 1. Frontend (Mobile App)

* Built with **React Native** and **Expo**
* Features camera integration, geolocation mapping, and media upload
* Styled using **NativeWind** (Tailwind CSS for React Native)

### 2. Backend (Main API)

* Built with **Node.js** and **Express**
* Uses **MongoDB** (via Mongoose) for database management
* Handles:

  * User authentication (JWT)
  * Secure routing
  * Media storage via **Cloudinary**

### 3. AI Microservice

* Built with **Python** and **FastAPI**
* **Image Classification:**

  * Uses Roboflow Inference SDK (YOLO/Detectron2)
* **Audio Processing:**

  * Uses Whisper for Speech-to-Text
  * NLP for processing voice-based reports

---

## ✨ Key Features

* **Capture & Report:** Take photos or record audio to report civic issues (e.g., potholes, broken streetlights)
* **Location Tagging:** Device location + interactive maps
* **AI Image Classification:** Detects issue type from images
* **AI Audio Processing:** Converts speech to structured data
* **Secure Authentication:** JWT-based system
* **Cloud Media Storage:** Uses Cloudinary

---

## 💻 Tech Stack

### Frontend (`/Frontend`)

* React Native / Expo
* React Navigation
* Axios
* NativeWind (Tailwind CSS)
* Expo Camera, Location, Image Picker, MapView

### Backend (`/Backend`)

* Node.js / Express.js
* MongoDB / Mongoose
* JSON Web Tokens (JWT)
* bcryptjs
* Multer & Cloudinary

### AI Microservice (`/ai-microservice`)

* Python 3.x
* FastAPI & Uvicorn
* Pydantic
* Roboflow Inference SDK
* Whisper (Speech-to-Text)

---

## 🚀 Getting Started

Follow these steps to run the project locally.

### 📌 Prerequisites

* Node.js (v16+)
* Python (3.8+)
* MongoDB (Local or Atlas)
* Expo CLI
* Cloudinary account

---

## 1️⃣ Backend Setup

```bash
cd Backend
npm install
```

Create a `.env` file in the Backend root:

```env
PORT=5000
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_api_key
CLOUDINARY_API_SECRET=your_api_secret
```

Start the backend:

```bash
npm run dev
```

---

## 2️⃣ AI Microservice Setup

```bash
cd ai-microservice
```

Create virtual environment (recommended):

```bash
python -m venv venv
source venv/bin/activate   # Windows: venv\\Scripts\\activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Create `.env` file for API keys (e.g., Roboflow).

Start server:

```bash
python ai-server.py
```

* Runs at: [http://0.0.0.0:5000](http://0.0.0.0:5000)
* Swagger Docs: [http://0.0.0.0:5000/docs](http://0.0.0.0:5000/docs)

---

## 3️⃣ Frontend Setup

```bash
cd Frontend
npm install
npm run start
```

* Scan QR with **Expo Go**
* Or run on emulator

---

## 📄 License

This project is licensed under the **MIT License**.
