# Deployment Instructions

This is a full-stack application with a React frontend and a Node.js/Express backend, using a PostgreSQL database.

## Prerequisites

- Node.js (v20+)
- PostgreSQL Database

## Local Development

1.  Install dependencies: `npm install`
2.  Set up your database and update `DATABASE_URL` in `.env`.
3.  Push the database schema: `npm run db:push`
4.  Start the development server: `npm run dev`

## Deployment (Production)

Since this application requires a running Node.js server and a PostgreSQL database, it is best deployed on platforms that support long-running processes (like Replit, Railway, Render, or Heroku).

### Option 1: Replit (Easiest)
1.  Simply use the "Run" button to start the app.
2.  For a permanent deployment, use Replit Deployments.

### Option 2: Railway / Render / Heroku
1.  **Build Command**: `npm run build`
2.  **Start Command**: `npm run start`
3.  **Environment Variables**:
    -   `DATABASE_URL`: Your PostgreSQL connection string.
    -   `PORT`: (Optional) The port to run on (default 5000).

### Note on Netlify/Vercel
Standard Netlify/Vercel deployments are optimized for static sites or serverless functions. To deploy this full Express backend on those platforms, you would typically need to refactor the `server/` code into serverless functions or use their specific "Web Frameworks" support if available. For this project, a standard Node.js host (like Replit or Railway) is recommended.
