# AI-Powered Quiz Platform with Knowledge Gap Tutor

An intelligent educational platform that combines interactive quizzes with AI-powered personalized learning recommendations for Biology, Chemistry, and Physics.

## 🌟 Features

### Student Portal
- **Student Login**: Secure login interface with demo access option
- **Personalized Dashboard**: Customized welcome message and quick access menu
- **Interactive Quizzes**: Multi-subject quiz system with instant feedback
- **Performance Results**: Detailed subject-wise performance analysis with percentages
- **AI Knowledge Gap Tutor**: Separate AI-powered analysis interface for personalized recommendations

### AI Analysis
- **Automated Performance Analysis**: AI evaluates quiz results and identifies weak areas
- **Personalized Recommendations**: Custom study suggestions based on performance
- **Smart Study Plans**: Daily time allocation for each subject
- **Knowledge Gap Identification**: Highlights specific areas needing improvement

## 📁 Project Structure

```
mrit/
├── STUDENT_LOGIN.html      # Student login page
├── STUDENTHOME.html         # Student dashboard
├── QUIZ.html                # Interactive quiz interface
├── RESULTS.html             # Performance results display
├── AI_TUTOR.html            # AI Knowledge Gap Tutor interface
├── HOME.html                # Home page
├── TUTORIAL.html            # Tutorial page
├── ai_analyzer.py           # AI analysis engine
├── api_server.py            # Flask API server
├── requirements.txt         # Python dependencies
└── start_servers.bat        # Server startup script (Windows)
```

## 🚀 Getting Started

### Prerequisites
- Python 3.7 or higher
- Modern web browser (Chrome, Firefox, Edge, Safari)

### Installation

1. **Install Python Dependencies**
   ```bash
   pip install -r requirements.txt
   ```

2. **Start the Servers**
   
   **Option A: Using Batch Script (Windows)**
   ```bash
   start_servers.bat
   ```

   **Option B: Manual Start**
   ```bash
   # Terminal 1 - Start AI API Server
   python api_server.py

   # Terminal 2 - Start Web Server
   python -m http.server 8000
   ```

3. **Access the Application**
   - Open your browser and navigate to: `http://localhost:8000/STUDENT_LOGIN.html`

## 🎯 User Journey

1. **Login**: Enter credentials or use "Continue as Demo Student"
2. **Dashboard**: Access various features from the student home page
3. **Take Quiz**: Answer questions from Biology, Chemistry, and Physics
4. **View Results**: Check subject-wise performance with percentages
5. **AI Analysis**: Visit AI Knowledge Gap Tutor for personalized recommendations

## 🛠️ Technology Stack

### Frontend
- HTML5, CSS3 (Gradients, Flexbox, Grid)
- JavaScript (ES6+, Fetch API, LocalStorage)

### Backend
- Python 3
- Flask 3.0.0 (Web Framework)
- Flask-CORS 4.0.0 (Cross-Origin Resource Sharing)

### Storage
- Browser LocalStorage for quiz data persistence

## 📊 API Endpoints

The AI API server runs on `http://localhost:5000` with the following endpoints:

- `POST /api/analyze` - Full performance analysis
- `POST /api/recommendations` - Get study recommendations
- `POST /api/study-plan` - Get personalized study plan
- `GET /api/health` - Health check

## 🎨 Customization

### Personalization
- Student greeting displays personalized name (e.g., "Welcome Bindu")
- AI agent named "AI KNOWLEDGE GAP TUTOR" in separate interface

### Color Scheme
- Primary gradient: Blue/Purple (#667eea → #764ba2)
- Subject colors:
  - Biology: Green (#4ade80 → #22c55e)
  - Chemistry: Blue (#60a5fa → #3b82f6)
  - Physics: Purple (#a78bfa → #8b5cf6)

## 📝 Key Features Details

### Quiz System
- Multiple choice questions from 3 subjects
- Real-time answer tracking
- LocalStorage-based data persistence
- Submit answers for evaluation

### Results Display
- Overall accuracy percentage
- Questions attempted count
- Individual subject cards with:
  - Percentage accuracy
  - Correct/Total/Wrong counts
  - Visual progress bars
  - Performance status indicators

### AI Knowledge Gap Tutor
- Separate dedicated interface
- API status indicator
- Performance summary dashboard
- "Analyze My Performance" button
- Displays:
  - AI-powered recommendations
  - Personalized study plans
  - Knowledge gap identification
  - Strengths and weaknesses analysis

## 🔧 Configuration

### Server Ports
- Web Server: Port 8000
- AI API Server: Port 5000

### Dependencies
```
flask==3.0.0
flask-cors==4.0.0
```

## 🐛 Troubleshooting

### Issue: Background not showing
- Ensure image file exists in the project root
- Hard refresh browser with `Ctrl + F5` (Windows) or `Cmd + Shift + R` (Mac)

### Issue: AI recommendations not displaying
- Verify both servers are running (ports 8000 and 5000)
- Check browser console for API connection errors
- Ensure Flask and Flask-CORS are installed

### Issue: Quiz results not saving
- Access via `http://localhost:8000` (not `file://`)
- Check browser LocalStorage is enabled
- Clear browser cache and retry

## 📄 License

This project is for educational purposes.

## 👥 Support

For issues or questions, refer to the application's built-in help section or contact your system administrator.

---

**Note**: This is a development server setup. For production deployment, use a production-grade WSGI server like Gunicorn or uWSGI.
