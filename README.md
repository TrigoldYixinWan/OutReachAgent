# Outreach Agent

A web-based application for finding contacts and sending automated personalized emails.

## Features

- 🔍 **Contact Sourcing**: Natural language search using Hunter.io API
- 🤖 **AI Summaries**: OpenAI-powered contact summaries
- 📧 **Email Integration**: Gmail OAuth for sending emails
- ✨ **Email Personalization**: AI-generated personalized email drafts

## Quick Start

### Prerequisites

- Node.js 18+
- Firebase project
- Google OAuth credentials
- Hunter.io API key
- OpenAI API key

### Backend Setup

1. Navigate to backend directory:
```bash
cd backend
```

2. Install dependencies:
```bash
npm install
```

3. Create `.env` file:
```env
PORT=8080
DEV_MODE=false
FIREBASE_PROJECT_ID=your-project-id

# APIs
HUNTER_API_KEY=your-hunter-api-key
OPENAI_API_KEY=your-openai-api-key

# Google OAuth
GOOGLE_CLIENT_ID=your-google-client-id
GOOGLE_CLIENT_SECRET=your-google-client-secret
GMAIL_REDIRECT_URI=http://localhost:8080/api/auth/gmail/callback
```

4. Add Firebase service account:
   - Download `firebase-service-account.json` from Firebase Console
   - Place it in `backend/` directory

5. Start server:
```bash
npm start
```

### Frontend Setup

1. Navigate to frontend directory:
```bash
cd frontend
```

2. Install dependencies:
```bash
npm install
```

3. Create `.env` file:
```env
VITE_BACKEND_URL=http://localhost:8080
VITE_FIREBASE_API_KEY=your-firebase-api-key
VITE_FIREBASE_AUTH_DOMAIN=your-project.firebaseapp.com
VITE_FIREBASE_PROJECT_ID=your-project-id
VITE_FIREBASE_STORAGE_BUCKET=your-project.appspot.com
VITE_FIREBASE_MESSAGING_SENDER_ID=your-sender-id
VITE_FIREBASE_APP_ID=your-app-id
```

4. Start development server:
```bash
npm run dev
```

## Usage

1. **Login**: Sign in with email/password or Google
2. **Find Contacts**: Use natural language search (e.g., "Find 10 engineers at Google")
3. **Accept Contacts**: Review and accept contacts you want to email
4. **Draft Emails**: Enter a template and generate personalized drafts
5. **Connect Gmail**: Authorize Gmail to send emails
6. **Send Emails**: Send individual or batch emails

## Project Structure

```
backend/
  src/
    controllers/    # Request handlers
    services/      # Business logic (Hunter, Gmail, OpenAI)
    routes/        # API routes
    config/        # Configuration (Firebase, CORS)
    middleware/    # Auth middleware

frontend/
  src/
    pages/         # Main pages (Login, Dashboard)
    components/    # Reusable components
    api/           # API clients
    config/        # Firebase config
```

## Environment Variables

See `.env.example` files in backend/ and frontend/ directories for required variables.

## Demo for core functionalities
### 1. Parsing Resume into formalized Profile Info
<img width="2550" height="1343" alt="Screenshot 2026-02-03 193915" src="https://github.com/user-attachments/assets/4a47ef91-ae5a-4f5d-8136-9d4b6086b7bd" />
<img width="2557" height="1341" alt="Screenshot 2026-02-03 193936" src="https://github.com/user-attachments/assets/e2ae47fe-32ad-48c2-8492-8068eacb084d" />

### 2. Searching recent uploaded job position and relevant HRs/insiders 
<img width="2553" height="1341" alt="Screenshot 2026-02-03 194010" src="https://github.com/user-attachments/assets/f9c837ae-5a46-4e4b-a57d-5aea9899169a" />
<img width="2549" height="1340" alt="Screenshot 2026-02-03 194035" src="https://github.com/user-attachments/assets/e90e3013-8582-4fe3-aa8f-56e9797a7f59" />

### 3. Auto-posish the Email according to your profile
<img width="2547" height="1330" alt="Screenshot 2026-02-03 221622" src="https://github.com/user-attachments/assets/f5707fa0-e31e-472b-a7fc-fd156a33bc54" />
<img width="2539" height="1339" alt="Screenshot 2026-02-03 221930" src="https://github.com/user-attachments/assets/2289dec9-4a79-45d2-a9cd-8c70f0a83376" />




