# Interview Practice Partner

An AI-powered agent helping users prepare for job interviews through mock interviews, real-time interaction, and detailed feedback.

## Features

- **Role-Specific Interviews**: Practice for Sales, Engineering, Retail, and General roles.
- **Voice Interaction**: Speak naturally with the AI using browser-based Speech-to-Text and Text-to-Speech.
- **Real-time Feedback**: Get instant responses and follow-up questions.
- **Performance Analysis**: Receive a detailed report on your strengths, weaknesses, and communication style after the interview.

## Tech Stack

- **Frontend**: Next.js 14 (App Router), React, TailwindCSS
- **AI**: Google Gemini (via `@google/generative-ai`)
- **Icons**: Lucide React
- **Styling**: TailwindCSS

## Setup Instructions

1. **Clone the repository**:
   ```bash
   git clone <repository-url>
   cd interview_prep
   ```

2. **Install dependencies**:
   ```bash
   npm install
   ```

3. **Configure Environment Variables**:
   - Copy `env.example` to `.env.local`:
     ```bash
     cp env.example .env.local
     ```
   - Add your Google Gemini API Key to `.env.local`:
     ```
     GEMINI_API_KEY=your_api_key_here
     ```

4. **Run the development server**:
   ```bash
   npm run dev
   ```

5. **Open the application**:
   Navigate to [http://localhost:3000](http://localhost:3000) in your browser.

## Architecture & Design Decisions

- **Next.js App Router**: Chosen for its robust routing and server-side capabilities, allowing for secure API route handling.
- **Web Speech API**: utilized for voice interaction to ensure zero-latency and zero-cost speech recognition and synthesis without external dependencies.
- **Google Gemini**: Selected for its fast inference and high-quality conversational abilities.
- **LocalStorage**: Used for persisting chat history across the session to generate feedback without a complex database setup for this MVP.

## Usage

1. Select a role from the landing page.
2. Allow microphone access when prompted.
3. Speak your answers or type them.
4. Click "End Interview" to receive your feedback report.
