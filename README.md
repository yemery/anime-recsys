# 🎌 Anime Recommendation System

<div align="center">

![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)
![Python](https://img.shields.io/badge/python-3.11-blue.svg)
![React](https://img.shields.io/badge/react-19.2.0-61dafb.svg)

A modern, full-stack anime recommendation system powered by machine learning. Discover your next favorite anime based on your preferences using content-based filtering and TF-IDF vectorization.

[Features](#-features) •
[Demo](#-demo) •
[Installation](#-installation) •
[Usage](#-usage) •
[API Documentation](#-api-documentation) •
[Contributing](#-contributing)

</div>

---

## 📖 Table of Contents

- [Overview](#-overview)
- [Features](#-features)
- [Architecture](#-architecture)
- [Tech Stack](#-tech-stack)
- [Prerequisites](#-prerequisites)
- [Installation](#-installation)
  - [Docker Setup (Recommended)](#docker-setup-recommended)
  - [Manual Setup](#manual-setup)
- [Usage](#-usage)
- [Project Structure](#-project-structure)
- [API Documentation](#-api-documentation)
- [Machine Learning Model](#-machine-learning-model)
- [Configuration](#-configuration)
- [Development](#-development)
- [Deployment](#-deployment)
- [Troubleshooting](#-troubleshooting)
- [Contributing](#-contributing)
- [License](#-license)
- [Acknowledgments](#-acknowledgments)

---

## 🌟 Overview

The Anime Recommendation System is a full-stack web application that leverages machine learning algorithms to provide personalized anime recommendations. By analyzing anime genres, synopses, and user preferences, the system suggests similar titles that users are likely to enjoy.

The application combines a FastAPI backend with a React frontend, utilizing modern web technologies and containerization for easy deployment and scalability.

### Key Highlights

- **ML-Powered Recommendations**: Uses TF-IDF vectorization and cosine similarity for content-based filtering
- **Real-time Anime Data**: Integrates with Jikan API (MyAnimeList unofficial API) for up-to-date anime information
- **Responsive UI**: Modern, mobile-friendly interface built with React and Ant Design
- **Dockerized**: Fully containerized application for consistent development and deployment
- **Scalable Architecture**: Microservices-based design with separate frontend and backend services

---

## ✨ Features

### For Users

- 🎯 **Personalized Recommendations**: Get tailored anime suggestions based on your favorite titles
- 🔍 **Advanced Search**: Filter anime by title, genre, type, and more
- 📱 **Responsive Design**: Seamless experience across desktop, tablet, and mobile devices
- 🎨 **Modern UI/UX**: Clean interface with Ant Design components and Tailwind CSS
- ⚡ **Fast Performance**: Optimized backend with caching and efficient ML algorithms
- 📊 **Detailed Information**: View comprehensive anime details including genres, synopsis, and ratings

### For Developers

- 🐳 **Docker Support**: Complete Docker Compose setup for easy local development
- 📚 **Well-Documented API**: RESTful API with FastAPI automatic documentation
- 🔧 **Hot Reload**: Automatic reloading for both frontend and backend during development
- 🧪 **ML Notebook**: Jupyter notebook included for model experimentation
- 🎓 **Clean Code**: Well-structured, modular codebase following best practices
- 🔐 **CORS Configured**: Pre-configured CORS middleware for seamless integration

---

## 🏗️ Architecture

```
┌─────────────────┐         ┌──────────────────┐         ┌─────────────────┐
│                 │         │                  │         │                 │
│  React Frontend │◄───────►│  FastAPI Backend │◄───────►│   Jikan API     │
│   (Port 5173)   │  HTTP   │   (Port 8000)    │  HTTP   │ (MyAnimeList)   │
│                 │         │                  │         │                 │
└─────────────────┘         └──────────────────┘         └─────────────────┘
                                     │
                                     │
                                     ▼
                            ┌──────────────────┐
                            │                  │
                            │  ML Recommender  │
                            │  (Scikit-learn)  │
                            │                  │
                            └──────────────────┘
                                     │
                                     │
                                     ▼
                            ┌──────────────────┐
                            │                  │
                            │  Anime Dataset   │
                            │    (CSV File)    │
                            │                  │
                            └──────────────────┘
```

---

## 🚀 Tech Stack

### Frontend

| Technology | Version | Purpose |
|------------|---------|---------|
| React | 19.2.0 | UI library for building interactive interfaces |
| Vite | 7.2.4 | Fast build tool and development server |
| React Router | 7.11.0 | Declarative routing for single-page application |
| Ant Design | 6.1.1 | Enterprise-grade UI component library |
| Tailwind CSS | 4.1.18 | Utility-first CSS framework |
| Axios | 1.13.2 | Promise-based HTTP client |
| Lucide React | 0.562.0 | Beautiful & consistent icon library |

### Backend

| Technology | Version | Purpose |
|------------|---------|---------|
| Python | 3.11 | Programming language |
| FastAPI | 0.127.0 | Modern, high-performance web framework |
| Pydantic | 2.12.5 | Data validation using Python type annotations |
| Scikit-learn | 1.8.0 | Machine learning library for recommendations |
| Pandas | 2.3.3 | Data manipulation and analysis |
| NumPy | 2.4.0 | Numerical computing library |
| Requests | 2.32.5 | HTTP library for API calls |
| Uvicorn | - | ASGI server for FastAPI |
| Python-dotenv | 1.2.1 | Environment variable management |

### Development & Deployment

- **Docker**: Containerization platform
- **Docker Compose**: Multi-container orchestration
- **Jupyter**: Interactive notebook for ML experimentation
- **ESLint**: JavaScript/React linting
- **Git**: Version control

---

## 📋 Prerequisites

Before you begin, ensure you have the following installed:

### For Docker Setup (Recommended)
- [Docker](https://www.docker.com/get-started) (version 20.10 or later)
- [Docker Compose](https://docs.docker.com/compose/install/) (version 2.0 or later)

### For Manual Setup
- [Node.js](https://nodejs.org/) (version 20 or later)
- [Python](https://www.python.org/) (version 3.11 or later)
- [pip](https://pip.pypa.io/en/stable/) (latest version)
- [npm](https://www.npmjs.com/) or [yarn](https://yarnpkg.com/) (latest version)

---

## 🛠️ Installation

### Docker Setup (Recommended)

This is the easiest way to get started. Docker will handle all dependencies and configuration.

1. **Clone the repository**
   ```bash
   git clone https://github.com/yemery/anime-recommendation-system.git
   cd anime-rec-sys
   ```

2. **Build and start the containers**
   ```bash
   docker-compose up --build
   ```

3. **Access the application**
   - Frontend: [http://localhost:5173](http://localhost:5173)
   - Backend API: [http://localhost:8000](http://localhost:8000)
   - API Documentation: [http://localhost:8000/docs](http://localhost:8000/docs)

4. **Stop the application**
   ```bash
   docker-compose down
   ```

> **Note**: The first build may take a few minutes as Docker downloads and installs all dependencies.

### Manual Setup

If you prefer to run the application without Docker:

#### Backend Setup

1. **Navigate to the backend directory**
   ```bash
   cd backend
   ```

2. **Create a virtual environment**
   ```bash
   # Windows
   python -m venv venv
   venv\Scripts\activate

   # macOS/Linux
   python3 -m venv venv
   source venv/bin/activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Set up environment variables** (optional)
   ```bash
   # Create a .env file
   echo "JIKAN_BASE_URL=https://api.jikan.moe/v4" > .env
   ```

5. **Run the backend server**
   ```bash
   uvicorn app.main:app --reload --host 0.0.0.0 --port 8000
   ```

   The backend will be available at [http://localhost:8000](http://localhost:8000)

#### Frontend Setup

1. **Open a new terminal and navigate to the frontend directory**
   ```bash
   cd frontend
   ```

2. **Install dependencies**
   ```bash
   npm install
   # or
   yarn install
   ```

3. **Set up environment variables** (optional)
   ```bash
   # Create a .env file
   echo "VITE_API_URL=http://localhost:8000" > .env
   ```

4. **Start the development server**
   ```bash
   npm run dev
   # or
   yarn dev
   ```

   The frontend will be available at [http://localhost:5173](http://localhost:5173)

---

## 💡 Usage

### Getting Recommendations

1. **Launch the application** using either Docker or manual setup
2. **Navigate to the homepage** at [http://localhost:5173](http://localhost:5173)
3. **Browse or search** for anime titles you like
4. **Select your favorite anime** from the list
5. **Click "Get Recommendations"** to receive personalized suggestions
6. **Explore the results** with detailed information about each recommended anime

### Using the API Directly

You can also interact with the API directly using tools like `curl`, Postman, or Python:

```bash
# Get anime recommendations
curl -X POST "http://localhost:8000/recommend" \
     -H "Content-Type: application/json" \
     -d '{
       "anime_list": ["Naruto", "Attack on Titan", "Death Note"],
       "top_n": 10
     }'

# Search for anime
curl "http://localhost:8000/anime?q=naruto&limit=5"

# Browse anime with pagination
curl "http://localhost:8000/anime?page=1&limit=12"
```

### Using Python

```python
import requests

# Get recommendations
response = requests.post(
    "http://localhost:8000/recommend",
    json={
        "anime_list": ["Naruto", "Attack on Titan", "Death Note"],
        "top_n": 10
    }
)
recommendations = response.json()

# Search for anime
response = requests.get(
    "http://localhost:8000/anime",
    params={"q": "naruto", "limit": 5}
)
anime_list = response.json()
```

---

## 📂 Project Structure

```
anime-rec-sys/
│
├── backend/                      # Backend FastAPI application
│   ├── app/
│   │   ├── __init__.py
│   │   ├── main.py              # FastAPI app entry point
│   │   └── recommender.py       # ML recommendation engine
│   ├── datasets/
│   │   └── anime.csv            # Anime dataset for ML model
│   ├── notebooks/
│   │   └── exploration_ml.ipynb # Jupyter notebook for ML experimentation
│   ├── Dockerfile               # Backend Docker configuration
│   └── requirements.txt         # Python dependencies
│
├── frontend/                     # Frontend React application
│   ├── public/                  # Static assets
│   ├── src/
│   │   ├── assets/              # Images, fonts, etc.
│   │   ├── components/          # Reusable React components
│   │   │   ├── atoms/           # Basic UI elements
│   │   │   ├── layout/          # Layout components
│   │   │   │   ├── AppLayout.jsx
│   │   │   │   ├── Footer.jsx
│   │   │   │   └── Navbar.jsx
│   │   │   └── molecules/       # Composite components
│   │   │       ├── AboutSection.jsx
│   │   │       ├── FeaturedAnime.jsx
│   │   │       ├── Footer.jsx
│   │   │       ├── HeroSection.jsx
│   │   │       └── HowItWorks.jsx
│   │   ├── pages/               # Page components
│   │   │   ├── Home.jsx
│   │   │   └── RecommendationPage.jsx
│   │   ├── routers/             # Routing configuration
│   │   │   └── AppRouter.jsx
│   │   ├── services/            # API service layer
│   │   │   ├── api.js           # Axios configuration
│   │   │   └── animeService.js  # Anime API calls
│   │   ├── App.css
│   │   ├── App.jsx              # Root component
│   │   ├── index.css
│   │   └── main.jsx             # Application entry point
│   ├── Dockerfile               # Frontend Docker configuration
│   ├── package.json             # Node.js dependencies
│   ├── vite.config.js           # Vite configuration
│   └── eslint.config.js         # ESLint configuration
│
├── docker-compose.yml           # Docker Compose orchestration
└── README.md                    # This file
```

---

## 📡 API Documentation

The backend provides a RESTful API with the following endpoints:

### Base URL
- Development: `http://localhost:8000`
- Production: Your deployed domain

### Endpoints

#### 1. Get Recommendations

**POST** `/recommend`

Get personalized anime recommendations based on a list of favorite anime.

**Request Body:**
```json
{
  "anime_list": ["Naruto", "Attack on Titan", "Death Note"],
  "top_n": 10
}
```

**Parameters:**
- `anime_list` (array, required): List of anime titles you like
- `top_n` (integer, optional): Number of recommendations to return (default: 10)

**Response:**
```json
{
  "input_anime": ["Naruto", "Attack on Titan", "Death Note"],
  "recommendations": [
    {
      "title": "Fullmetal Alchemist: Brotherhood",
      "genres": "Action, Adventure, Drama, Fantasy",
      "synopsis": "After a horrific alchemy experiment goes wrong..."
    },
    {
      "title": "Code Geass",
      "genres": "Action, Drama, Mecha, Sci-Fi",
      "synopsis": "The Empire of Britannia has invaded Japan..."
    }
  ]
}
```

**Status Codes:**
- `200 OK`: Successful recommendation
- `422 Unprocessable Entity`: Invalid request body

#### 2. Get Anime List

**GET** `/anime`

Retrieve a paginated list of anime with optional filtering.

**Query Parameters:**
- `page` (integer, optional): Page number (default: 1, minimum: 1)
- `limit` (integer, optional): Results per page (default: 12, maximum: 24)
- `q` (string, optional): Search query for anime title
- `type` (string, optional): Filter by anime type (TV, Movie, OVA, etc.)

**Example Request:**
```bash
GET /anime?page=1&limit=12&q=naruto&type=TV
```

**Response:**
```json
{
  "pagination": {
    "last_visible_page": 10,
    "has_next_page": true,
    "current_page": 1,
    "items": {
      "count": 12,
      "total": 120,
      "per_page": 12
    }
  },
  "data": [
    {
      "mal_id": 20,
      "title": "Naruto",
      "images": { ... },
      "synopsis": "...",
      "type": "TV",
      "episodes": 220,
      "score": 7.99
    }
  ]
}
```

**Status Codes:**
- `200 OK`: Successful request
- `502 Bad Gateway`: External API error

### Interactive API Documentation

FastAPI provides automatic interactive documentation:

- **Swagger UI**: [http://localhost:8000/docs](http://localhost:8000/docs)
- **ReDoc**: [http://localhost:8000/redoc](http://localhost:8000/redoc)

These interfaces allow you to test the API directly from your browser.

---

## 🤖 Machine Learning Model

### Algorithm Overview

The recommendation system uses **Content-Based Filtering** with the following approach:

1. **Feature Engineering**: Combines anime genres and synopsis into a single text feature
2. **TF-IDF Vectorization**: Converts text features into numerical vectors
3. **Cosine Similarity**: Calculates similarity scores between anime
4. **Collaborative Filtering**: Averages similarity scores from multiple input anime

### Technical Details

```python
# Feature combination
combined_features = genres + " " + synopsis

# TF-IDF Vectorization
- stop_words: 'english'
- max_features: 5000

# Similarity calculation
cosine_similarity(anime_vectors)
```

### Model Performance

- **Dataset Size**: Thousands of anime titles
- **Feature Dimensions**: 5000 TF-IDF features
- **Average Response Time**: < 100ms for 10 recommendations
- **Accuracy**: Based on genre and content similarity

### Customizing the Model

To experiment with the model, use the Jupyter notebook:

```bash
# Start Jupyter
cd backend/notebooks
jupyter notebook exploration_ml.ipynb
```

You can adjust:
- TF-IDF parameters (max_features, ngram_range, etc.)
- Similarity metrics (cosine, euclidean, etc.)
- Feature combinations
- Weighting schemes

---

## ⚙️ Configuration

### Environment Variables

#### Backend (.env)

```bash
# Jikan API Configuration
JIKAN_BASE_URL=https://api.jikan.moe/v4

# Server Configuration (optional)
HOST=0.0.0.0
PORT=8000
```

#### Frontend (.env)

```bash
# API Configuration
VITE_API_URL=http://localhost:8000

# Other Vite variables
VITE_APP_NAME=Anime Recommendation System
```

### Docker Configuration

#### Backend Service (docker-compose.yml)

```yaml
backend:
  ports:
    - "8000:8000"
  environment:
    - JIKAN_BASE_URL=https://api.jikan.moe/v4
  volumes:
    - ./backend:/app
```

#### Frontend Service (docker-compose.yml)

```yaml
frontend:
  ports:
    - "5173:5173"
  environment:
    - VITE_API_URL=http://localhost:8000
  volumes:
    - ./frontend:/app
```

---

## 🔧 Development

### Running in Development Mode

**With Docker:**
```bash
# Start with auto-reload enabled
docker-compose up

# View logs
docker-compose logs -f

# Restart specific service
docker-compose restart backend
```

**Without Docker:**
```bash
# Backend (with hot reload)
cd backend
uvicorn app.main:app --reload

# Frontend (with hot reload)
cd frontend
npm run dev
```

### Code Formatting & Linting

**Frontend:**
```bash
# Run ESLint
npm run lint

# Fix linting issues
npm run lint -- --fix
```

**Backend:**
```bash
# Format with black
black app/

# Sort imports
isort app/

# Type checking
mypy app/
```

### Adding New Dependencies

**Backend:**
```bash
# Install package
pip install package-name

# Update requirements.txt
pip freeze > requirements.txt
```

**Frontend:**
```bash
# Install package
npm install package-name

# Or for dev dependencies
npm install --save-dev package-name
```

### Database Updates

To update the anime dataset:

1. Download new CSV from [Kaggle](https://www.kaggle.com/) or other sources
2. Replace `backend/datasets/anime.csv`
3. Restart the backend service to reload the model

---

## 🚢 Deployment

### Docker Deployment

For production deployment, modify the Dockerfiles to use production builds:

**Frontend (Production Dockerfile):**
```dockerfile
FROM node:20-alpine AS builder
WORKDIR /app
COPY package*.json ./
RUN npm ci
COPY . .
RUN npm run build

FROM nginx:alpine
COPY --from=builder /app/dist /usr/share/nginx/html
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
```

**Backend (Production Dockerfile):**
```dockerfile
FROM python:3.11-slim
WORKDIR /app
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt
COPY . .
EXPOSE 8000
CMD ["uvicorn", "app.main:app", "--host", "0.0.0.0", "--port", "8000", "--workers", "4"]
```

### Deployment Platforms

The application can be deployed to:

- **AWS**: ECS, EC2, or Elastic Beanstalk
- **Google Cloud**: Cloud Run or Kubernetes Engine
- **Azure**: Container Instances or App Service
- **Heroku**: Using Docker containers
- **DigitalOcean**: App Platform or Droplets
- **Vercel/Netlify**: Frontend only (requires separate backend)

### Environment Configuration

For production, ensure you set:

1. Secure environment variables
2. CORS origins to your domain only
3. API rate limiting
4. HTTPS/SSL certificates
5. Database persistence (if using databases)
6. Logging and monitoring

---

## 🔍 Troubleshooting

### Common Issues

#### Port Already in Use

**Problem**: `Error: Address already in use`

**Solution**:
```bash
# Find process using port
# Windows
netstat -ano | findstr :8000
taskkill /PID <PID> /F

# macOS/Linux
lsof -i :8000
kill -9 <PID>
```

#### Docker Container Fails to Start

**Problem**: Container exits immediately

**Solution**:
```bash
# Check logs
docker-compose logs backend

# Rebuild containers
docker-compose down
docker-compose up --build
```

#### Module Not Found Error

**Problem**: `ModuleNotFoundError: No module named 'app'`

**Solution**:
```bash
# Ensure you're in the correct directory
cd backend

# Reinstall dependencies
pip install -r requirements.txt

# Or rebuild Docker
docker-compose up --build
```

#### API CORS Errors

**Problem**: CORS policy blocking requests

**Solution**: Update CORS settings in `backend/app/main.py`:
```python
app.add_middleware(
    CORSMiddleware,
    allow_origins=["http://localhost:5173", "your-domain.com"],
    allow_credentials=False,
    allow_methods=["GET", "POST", "OPTIONS"],
    allow_headers=["*"],
)
```

#### Jikan API Rate Limiting

**Problem**: Too many requests to Jikan API

**Solution**: Implement rate limiting or caching:
```python
import time
from functools import lru_cache

@lru_cache(maxsize=128)
def get_anime_cached(url):
    time.sleep(1)  # Rate limiting
    return requests.get(url)
```

---

## 🤝 Contributing

Contributions are welcome and appreciated! Here's how you can contribute:

### Getting Started

1. **Fork the repository**
   ```bash
   # Click "Fork" on GitHub
   ```

2. **Clone your fork**
   ```bash
   git clone https://github.com/your-username/anime-recommendation-system.git
   cd anime-rec-sys
   ```

3. **Create a feature branch**
   ```bash
   git checkout -b feature/amazing-feature
   ```

4. **Make your changes**
   - Write clean, readable code
   - Follow existing code style
   - Add comments where necessary
   - Update documentation

5. **Test your changes**
   ```bash
   # Test backend
   cd backend
   pytest

   # Test frontend
   cd frontend
   npm run test
   ```

6. **Commit your changes**
   ```bash
   git add .
   git commit -m "Add: Amazing new feature"
   ```

7. **Push to your fork**
   ```bash
   git push origin feature/amazing-feature
   ```

8. **Open a Pull Request**
   - Go to the original repository
   - Click "New Pull Request"
   - Describe your changes

### Contribution Guidelines

- **Code Style**: Follow PEP 8 for Python, ESLint rules for JavaScript
- **Commits**: Use clear, descriptive commit messages
- **Documentation**: Update README and docstrings
- **Testing**: Add tests for new features
- **Issues**: Check existing issues before creating new ones

### Areas to Contribute

- 🐛 Bug fixes
- ✨ New features
- 📝 Documentation improvements
- 🎨 UI/UX enhancements
- 🧪 Test coverage
- 🌐 Translations
- ⚡ Performance optimizations

---

## 📄 License

This project is licensed under the MIT License - see below for details:

```
MIT License

Copyright (c) 2026 Yemery

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## 🙏 Acknowledgments

This project was made possible by the following amazing resources and communities:

### APIs & Data Sources
- **[Jikan API](https://jikan.moe/)** - Unofficial MyAnimeList API for anime data
- **[MyAnimeList](https://myanimelist.net/)** - Comprehensive anime database
- **[Kaggle](https://www.kaggle.com/)** - Dataset sources for machine learning

### Technologies & Libraries
- **[FastAPI](https://fastapi.tiangolo.com/)** - Modern Python web framework
- **[React](https://react.dev/)** - JavaScript library for building user interfaces
- **[Ant Design](https://ant.design/)** - Enterprise UI component library
- **[Scikit-learn](https://scikit-learn.org/)** - Machine learning in Python
- **[Docker](https://www.docker.com/)** - Containerization platform

### Inspiration & Learning
- **[freeCodeCamp](https://www.freecodecamp.org/)** - Web development tutorials
- **[YouTube Tutorials](https://www.youtube.com/)** - Various programming guides
- **[Stack Overflow](https://stackoverflow.com/)** - Developer community support
- **[GitHub](https://github.com/)** - Code hosting and collaboration

### Special Thanks
- All contributors who help improve this project
- The open-source community for amazing tools and libraries
- Anime fans who inspired this project

---

## 📞 Contact & Support

### Get in Touch

- **GitHub**: [@yemery](https://github.com/yemery)
- **Repository**: [anime-recommendation-system](https://github.com/yemery/anime-recommendation-system)
- **Issues**: [Report a bug or request a feature](https://github.com/yemery/anime-recommendation-system/issues)

### Support This Project

If you find this project helpful, please consider:

- ⭐ Starring the repository
- 🐛 Reporting bugs
- 💡 Suggesting new features
- 🤝 Contributing code
- 📢 Sharing with others

---

<div align="center">

Made with ❤️ by [Yemery](https://github.com/yemery)

**[⬆ Back to Top](#-anime-recommendation-system)**

</div>



