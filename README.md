# CivicSight AI

**CivicSight AI** is an AI-powered citizen issue reporting system. It allows users to capture and report civic issues using images or voice notes, which are then automatically classified and processed using machine learning models.

## 🏗️ Project Architecture

This project is built using a modern microservices-inspired architecture, consisting of three main components:

1. **Frontend (Mobile App)**
   - Built with **React Native** and **Expo**.
   - Features camera integration, geolocation mapping, and media upload.
   - Styled using **NativeWind** (Tailwind CSS for React Native).

2. **Backend (Main API)**
   - Built with **Node.js** and **Express**.
   - Uses **MongoDB** (via Mongoose) for database management.
   - Handles user authentication (JWT), secure routing, and media storage integration via **Cloudinary**.

3. **AI Microservice**
   - Built with **Python** and **FastAPI**.
   - **Image Classification:** Uses Roboflow's Inference SDK (YOLO/Detectron2) to analyze and classify uploaded images of civic issues.
   - **Audio Processing:** Uses Whisper for Speech-to-Text and NLP to process voice-based issue reports.

---

## ✨ Key Features

* **Capture & Report:** Users can take photos or record audio to report local civic issues (e.g., potholes, broken streetlights).
* **Location Tagging:** Integrates with device location and interactive maps to pinpoint issues.
* **AI Image Classification:** Automatically detects the type of civic issue from image payloads.
* **AI Audio Processing:** Transcribes voice notes and structures the reported data automatically.
* **Secure Authentication:** JWT-based user authentication and secure data handling.
* **Cloud Media Storage:** Direct upload of media assets to Cloudinary.

---

## 💻 Tech Stack

**Frontend (`/Frontend`)**
- React Native / Expo
- React Navigation
- Axios
- NativeWind (Tailwind CSS)
- Expo Camera, Location, Image Picker, and MapView

**Backend (`/Backend`)**
- Node.js / Express.js
- MongoDB / Mongoose
- JSON Web Tokens (JWT) & bcryptjs
- Multer & Cloudinary

**AI Microservice (`/ai-microservice`)**
- Python 3.x
- FastAPI & Uvicorn
- Pydantic
- Roboflow Inference SDK
- Whisper (Speech-to-Text)

---

## 🚀 Getting Started

Follow these instructions to get the project up and running on your local machine.

### Prerequisites
- Node.js (v16.0.0 or higher)
- Python (3.8 or higher)
- MongoDB instance (local or Atlas)
- Expo CLI
- Cloudinary Account

### 1. Backend Setup
1. Navigate to the backend directory:
   ```bash
   cd Backend
Install dependencies:

Bash
npm install
Create a .env file in the Backend root and add your environment variables:

Code snippet
PORT=5000
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_api_key
CLOUDINARY_API_SECRET=your_api_secret
Start the development server:

Bash
npm run dev
2. AI Microservice Setup
Navigate to the AI microservice directory:

Bash
cd ai-microservice
Create a virtual environment (optional but recommended):

Bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
Install dependencies:

Bash
pip install -r requirements.txt
Create a .env file for your AI API keys (e.g., Roboflow keys).

Start the FastAPI server:

Bash
python ai-server.py
# Starts automatically on [http://0.0.0.0:5000](http://0.0.0.0:5000) 
Note: Interactive API docs will be available at /docs (Swagger UI).

3. Frontend Setup
Navigate to the frontend directory:

Bash
cd Frontend
Install dependencies:

Bash
npm install
Start the Expo development server:

Bash
npm run start
Use the Expo Go app on your phone to scan the QR code, or run it on an iOS/Android emulator.

📄 License
This project is licensed under the MIT License.
