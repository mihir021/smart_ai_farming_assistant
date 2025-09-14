Krishi Mitra - Farmer Assistant Platform
=======================================

A Flask-based web application that helps farmers with:
- Account creation and login (secure with JWT & bcrypt)
- Personalized chatbot assistance (Hindi/Gujarati)
- Weather forecast & crop suggestions
- Government schemes & news
- Farmer dashboard and offline support

-------------------------------------------------------
Features
-------------------------------------------------------
- User Authentication
  * Signup & Login using email/password
  * Passwords stored securely with bcrypt
  * JWT-based token authentication

- AI-Powered Chatbot
  * Uses OpenAI gpt-4o-mini
  * Answers queries in Hindi or Gujarati
  * Role-based system instructions for farming support

- Crop Suggestion API
  * Takes location as input
  * Generates a 7-day weather forecast
  * Suggests suitable crops based on weather & soil

- Government News API
  * Returns latest schemes, policies, and farmer-related news
  * AI outputs structured JSON with title & description

- Frontend Pages
  * Login, Create Account, Welcome, Dashboard
  * Chatbot, Crop Suggestions, Govt Schemes, Offline Mode

-------------------------------------------------------
Tech Stack
-------------------------------------------------------
- Backend: Flask (Python)
- Frontend: HTML + Jinja2 Templates
- Security: JWT, bcrypt
- AI: OpenAI GPT models
- Environment: .env for secrets

-------------------------------------------------------
Installation & Setup
-------------------------------------------------------
1. Clone the repository:
   git clone https://github.com/yourusername/krishi-mitra.git
   cd krishi-mitra

2. Create virtual environment & install dependencies:
   python -m venv venv
   source venv/bin/activate   # For Linux/Mac
   venv\Scripts\activate      # For Windows
   pip install -r requirements.txt

3. Setup environment variables (.env file):
   OPENAI_API_KEY=sk-xxxxxxxxxxxxxxxxxxxx
   JWT_SECRET_KEY=your-secret-key

4. Run the server:
   python app.py

5. Visit in Browser:
   http://127.0.0.1:5000/

-------------------------------------------------------
API Endpoints
-------------------------------------------------------
Auth:
- POST /api/auth/signup → Create account
- POST /api/auth/login → Login and get JWT token

Chatbot:
- POST /chat
  { "message": "खेती के लिए क्या सुझाव है?" }

Crop Suggestion:
- POST /api/crop-suggestion
  { "location": "Ahmedabad" }

Govt News:
- GET /api/govt-news
  { "news": [ { "title": "PM Kisan Yojana", "description": "Farmers get ₹6000 annually..." } ] }

-------------------------------------------------------
Security Notes
-------------------------------------------------------
- Never commit .env file to GitHub
- Rotate API keys if exposed
- Use HTTPS in production

-------------------------------------------------------
License
-------------------------------------------------------
This project is licensed under the MIT License.
