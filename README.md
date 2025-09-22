# AI Medical Doctor

A cutting-edge, full-stack medical consultation platform powered by advanced AI technologies. This application provides instant medical analysis through voice recognition, medical image analysis, and professional AI-generated responses with ICD-10 medical codes.

## 🌟 Features

### 🤖 AI-Powered Medical Analysis
- **Medical Image Analysis**: Upload X-rays, MRIs, CT scans, skin conditions, or any medical images for instant AI-powered diagnostic insights
- **Voice-to-Text Recognition**: Record symptoms naturally using advanced speech recognition technology
- **Professional AI Responses**: Get structured medical insights with differential diagnoses and ICD-10 medical codes
- **Audio Doctor Responses**: Listen to AI-generated doctor responses with natural voice synthesis

### 💻 Technology Highlights
- **Advanced AI Models**: Groq Llama 4 Scout 17B for image analysis, Whisper Large V3 for speech recognition
- **Premium Audio**: ElevenLabs for high-quality text-to-speech with Google TTS fallback
- **Modern Frontend**: React 19 with TypeScript, Tailwind CSS, and responsive design
- **Robust Backend**: FastAPI with async support, comprehensive error handling, and RESTful APIs
- **Professional UI/UX**: Medical-themed interface with glassmorphism effects and smooth animations

## 🏗️ Architecture Overview

```
AI-Medical-Doctor/
├── 🖥️  frontend/              # React 19 + TypeScript Application
│   ├── src/
│   │   ├── components/        # React Components
│   │   │   ├── LandingPage.tsx         # Professional homepage
│   │   │   ├── ConsultationPage.tsx    # Main consultation interface
│   │   │   └── MedicalAICards.tsx      # Feature showcase
│   │   ├── services/
│   │   │   └── api.ts         # Backend API integration
│   │   ├── App.tsx           # Main app with routing
│   │   └── index.css         # Tailwind + custom styles
│   ├── public/               # Static assets
│   ├── package.json          # Dependencies & scripts
│   └── tailwind.config.js    # UI configuration
│
├── 🔧  backend/               # FastAPI Python Server
│   ├── main.py               # FastAPI app & API endpoints
│   ├── brain_of_doc.py       # AI image analysis (Groq/Llama)
│   ├── voice_of_patient.py   # Speech-to-text processing
│   ├── voice_of_doctor.py    # Text-to-speech generation
│   ├── requirements.txt      # Python dependencies
│   └── .env.example         # Environment template
│
├── 📁 Root Files
│   ├── .gitignore           # Comprehensive git ignore
│   ├── build.sh             # Build automation script
│   └── README.md            # This documentation
```

## 🚀 Quick Start Guide

### 📋 Prerequisites

- **Node.js** 16.0+ and npm
- **Python** 3.8+
- **API Keys** (required):
  - **GROQ_API_KEY**: For image analysis and speech transcription
  - **ELEVENLABS_API_KEY**: For premium TTS (optional, falls back to Google TTS)

### 🔧 Installation & Setup

#### 1. Clone the Repository
```bash
git clone <repository-url>
cd Ai-Medical-Doctor
```

#### 2. Backend Setup
```bash
# Navigate to backend directory
cd backend

# Create virtual environment
python -m venv venv

# Activate virtual environment
# macOS/Linux:
source venv/bin/activate
# Windows:
# venv\Scripts\activate

# Install Python dependencies
pip install -r requirements.txt

# Setup environment variables
cp .env.example .env
# Edit .env file with your API keys:
# GROQ_API_KEY=your_groq_api_key_here
# ELEVENLABS_API_KEY=your_elevenlabs_api_key_here
```

#### 3. Frontend Setup
```bash
# Navigate to frontend directory (from root)
cd frontend

# Install Node.js dependencies
npm install
# or
yarn install
```

#### 4. Start the Application
```bash
# Terminal 1 - Start Backend Server
cd backend
uvicorn main:app --reload --host 0.0.0.0 --port 8000

# Terminal 2 - Start Frontend Server
cd frontend
npm start
```

### 🌐 Access the Application
- **Frontend**: http://localhost:3000
- **Backend API**: http://localhost:8000
- **API Documentation**: http://localhost:8000/docs

## 🛠️ Technology Stack

### Backend Technologies
| Component | Technology | Purpose |
|-----------|------------|---------|
| **Web Framework** | FastAPI | High-performance async API server |
| **AI Image Analysis** | Groq Llama 4 Scout 17B | Medical image interpretation |
| **Speech Recognition** | Whisper Large V3 | Audio-to-text transcription |
| **Text-to-Speech** | ElevenLabs + Google TTS | Natural voice generation |
| **Audio Processing** | PyDub, SpeechRecognition | Audio file handling |
| **Image Processing** | Pillow, Base64 | Medical image processing |
| **Server** | Uvicorn | ASGI server implementation |

### Frontend Technologies
| Component | Technology | Purpose |
|-----------|------------|---------|
| **Framework** | React 19.1.1 | Modern UI framework |
| **Language** | TypeScript 4.9.5 | Type-safe development |
| **Styling** | Tailwind CSS 3.4 | Utility-first styling |
| **Routing** | React Router DOM 7.8.2 | SPA navigation |
| **HTTP Client** | Axios 1.11.0 | API communication |
| **Icons** | Lucide React 0.542.0 | Professional icon set |
| **Build Tool** | Create React App 5.0.1 | Development toolchain |

## 🎯 Core Functionality

### 🖼️ Medical Image Analysis
Upload medical images including:
- **Radiology**: X-rays, MRIs, CT scans, ultrasounds
- **Dermatology**: Skin conditions, rashes, lesions
- **Pathology**: Tissue samples, lab results
- **General**: Any medical photograph or scan

**AI Capabilities**:
- Detailed medical image interpretation
- Differential diagnosis suggestions
- ICD-10 medical code matching
- Treatment recommendations
- Professional medical language

### 🎙️ Voice Recognition System
- **Real-time Recording**: Browser-based audio capture
- **Advanced Transcription**: Groq Whisper Large V3 model
- **Medical Terminology**: Optimized for healthcare vocabulary
- **Multiple Formats**: WAV, MP3, and other audio formats
- **Error Handling**: Microphone permission management

### 🔊 Text-to-Speech Synthesis
- **Premium Quality**: ElevenLabs Aria voice for natural speech
- **Medical Pronunciation**: Accurate medical term pronunciation
- **Fallback System**: Google TTS for reliability
- **Audio Controls**: Play, pause, and volume control
- **Multiple Formats**: MP3 output for broad compatibility

## 📱 User Interface

### 🏠 Landing Page (`/`)
- **Hero Section**: Professional medical branding with animated icons
- **Feature Overview**: Three main capabilities with detailed descriptions
- **Responsive Design**: Mobile-first approach with touch-friendly interface
- **Professional Navigation**: Clean header with mobile hamburger menu
- **Call-to-Action**: Direct routing to consultation interface

### 🏥 Consultation Page (`/consultation`)
- **Audio Recording Interface**: 
  - Visual recording indicators
  - Real-time microphone feedback
  - Recording controls with accessibility
- **Image Upload System**:
  - Drag-and-drop functionality
  - Click-to-upload alternative
  - Instant image preview with removal options
- **Results Display**:
  - Structured transcription display
  - Professional medical analysis formatting
  - Audio playback controls for doctor responses
- **Error Handling**: User-friendly error messages and recovery options



