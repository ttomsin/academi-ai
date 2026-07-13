# AI Study Planner & Assistant

This is a full-stack study assistant application built with React, Vite, Tailwind CSS, Express, and Supabase. It uses the Gemini API to analyze syllabuses, extract text from course materials (PDFs), generate personalized study notes, and create step-by-step study plans.

## Features
- **Authentication**: User signup and login powered by Supabase Auth.
- **Dashboard & Gamification**: Track tasks, earn points, maintain streaks, and level up.
- **Course Management**: Manage courses and view detailed course information.
- **AI Material Parsing**: Upload PDFs and automatically extract text.
- **AI Study Notes & Plans**: Generate personalized study notes and actionable study plans from course materials using Gemini 2.5 Flash.
- **Task Management**: Automatically convert study plan steps into tasks.
- **Leaderboard**: Compete with other students for the top spot.

## Prerequisites

To run this application, you will need:
- [Node.js](https://nodejs.org/) (v18 or higher recommended)
- A [Supabase](https://supabase.com/) project (for PostgreSQL database and Authentication)
- A [Google Gemini API Key](https://aistudio.google.com/)

## Setup & Installation

1. **Clone the repository** (if you haven't already):
   ```bash
   git clone <repository-url>
   cd <project-directory>
   ```

2. **Install dependencies**:
   ```bash
   npm install
   ```

3. **Database Setup (Supabase)**:
   - Create a new project in Supabase.
   - Go to the SQL Editor in your Supabase dashboard.
   - Copy the contents of the `database.sql` file in this repository and run it in the SQL Editor. This will set up all the necessary tables, Row Level Security (RLS) policies, and triggers.

4. **Environment Variables**:
   - Rename `.env.example` to `.env` or create a new `.env` file in the root directory.
   - Fill in the required credentials:
     ```env
     # Your Google Gemini API Key
     GEMINI_API_KEY=your_gemini_api_key_here
     
     # Your Supabase Project Credentials
     VITE_SUPABASE_URL=your_supabase_project_url
     VITE_SUPABASE_ANON_KEY=your_supabase_anon_key
     ```

## Running the Application

To start the development server (which starts both the Express backend and the Vite frontend):

```bash
npm run dev
```

The application will typically be available at `http://localhost:3000`.

## Building for Production

To build the project for production:

```bash
npm run build
```

This will compile the frontend assets into the `dist/` directory and build the backend server. To start the production server:

```bash
npm run start
```
