# 🚀 AI Multimodal Search Foundation Model

![Python](https://img.shields.io/badge/Python-3.9+-blue.svg)
![FastAPI](https://img.shields.io/badge/FastAPI-0.95+-green.svg)
![React](https://img.shields.io/badge/React-18.2+-blue.svg)
![Tailwind](https://img.shields.io/badge/Tailwind-3.0+-38B2AC.svg)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-15+-336791.svg)
![Gemini](https://img.shields.io/badge/Gemini-API-4285F4.svg)
![Docker](https://img.shields.io/badge/Docker-24.0+-2496ED.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)

> 🔍 **Unified Search Across Images, Audio, Videos, Documents & Code** using Google's Gemini API and Vector Embeddings

## 📌 Overview

A powerful multimodal search system that breaks down barriers between different media types by creating a **unified semantic understanding** of all content. This project demonstrates how AI can understand and search across images, audio, videos, documents, and source code using the same conceptual framework.

### 🎯 Key Features

- 🖼️ **Image Search**: Find images using text descriptions
- 🎵 **Audio Search**: Discover audio files by content description
- 🎬 **Video Search**: Search videos by scene description
- 📄 **Document Search**: Find documents by semantic meaning
- 💻 **Code Search**: Search code repositories by functionality
- 🔍 **Cross-Modal Search**: "Show me sunsets" finds images, videos, and audio
- 🎨 **Modern UI**: Beautiful, responsive interface with dark/light mode
- ⚡ **Real-Time**: Instant embedding generation and search results

## 🧠 How It Works

### Core Architecture



### Process Flow

1. **Upload**: User uploads any file (image, audio, video, document, code)
2. **Process**: File is validated and processed
3. **Embed**: Gemini API generates vector embedding
4. **Store**: Embedding stored in PostgreSQL with pgvector
5. **Search**: User enters query → converted to embedding → similar vectors found
6. **Results**: Ranked results displayed with preview

## 🛠️ Technology Stack

### Backend
| Technology | Purpose |
|------------|---------|
| **FastAPI** | High-performance API framework |
| **Google Gemini API** | Multi-modal embedding generation |
| **PostgreSQL + pgvector** | Vector storage and similarity search |
| **Redis** | Caching for frequent queries |
| **SQLAlchemy** | ORM for database operations |
| **Pillow, PyPDF2** | File processing |
| **Python 3.9+** | Backend language |

### Frontend
| Technology | Purpose |
|------------|---------|
| **React 18** | UI framework |
| **React Router** | Navigation |
| **Tailwind CSS** | Styling framework |
| **Framer Motion** | Animations |
| **Axios** | API calls |
| **React Dropzone** | Drag-and-drop upload |
| **React Hook Form** | Form handling |
| **Recharts** | Data visualization |

### Database
| Technology | Purpose |
|------------|---------|
| **PostgreSQL 15** | Primary database |
| **pgvector** | Vector similarity search |
| **Redis** | Caching layer |

## 📁 Project Structure



## 🚀 Quick Start

### Prerequisites

- Python 3.9+
- Node.js 18+
- PostgreSQL 15+
- Docker (optional)
- Gemini API Key ([Get it here](https://ai.google.dev/))

### Installation

#### 1. Clone the Repository

```bash
git clone https://github.com/vishakha2121/AI-Multimodal-Search-Foundation-Model.git
cd AI-Multimodal-Search-Foundation-Model

# Create virtual environment
cd backend
python -m venv venv

# Activate virtual environment
# On Windows:
venv\Scripts\activate
# On Mac/Linux:
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Create .env file
cp .env.example .env

# Edit .env and add your Gemini API key
# GEMINI_API_KEY=your_api_key_here

# Run database migrations
python -m app.database.migrations

# Start backend server
uvicorn app.main:app --reload --host 0.0.0.0 --port 8000

# Open new terminal
cd frontend

# Install dependencies
npm install

# Create .env file
cp .env.example .env

# Start development server
npm start
# Open new terminal
cd frontend

# Install dependencies
npm install

# Create .env file
cp .env.example .env

# Start development server
npm start
