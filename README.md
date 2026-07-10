# QuirkLink
 
QuirkLink is a fast, minimal URL shortener built to turn long, messy links into clean, shareable ones — built as a hands-on project to explore full-stack development with Next.js and MongoDB.
 
## What is QuirkLink?
 
QuirkLink takes any long URL and generates a short, custom link in seconds. Under the hood, it combines server-side API routes, a NoSQL database, and serverless deployment into one clean, production-ready flow — no separate backend server required.
 
## Tech Stack
 
- **Frontend:** Next.js, React
- **Backend/API:** Next.js API Routes (App Router)
- **Database:** MongoDB (Atlas)
- **Deployment:** Vercel
## How It Works
 
1. **Client Interface:** Users enter a long URL and a custom short URL through the Next.js frontend.
2. **API Communication:** The frontend sends a POST request to the `/api/generate` route.
3. **Data Management:** The backend checks MongoDB for a duplicate short URL, then stores the new URL pair securely in the database.
4. **Redirection:** Visiting a short URL looks it up in MongoDB and redirects to the original long URL.
## Architecture Flow
 
```
User → Next.js Frontend → /api/generate (API Route) → MongoDB Atlas
                                                              ↓
                                                    Stores { url, shorturl }
```
 
## Getting Started
 
To run this project locally:
 
1. Install dependencies:
```bash
npm install
```
 
2. Add your MongoDB connection string to a `.env.local` file:
```
MONGODB_URI=your_mongodb_connection_string
```
 
3. Start the development server:
```bash
npm run dev
```
 
4. Open [http://localhost:3000](http://localhost:3000) to view it in the browser.
## Deployment
 
This project is deployed on [Vercel](https://vercel.com). To deploy your own version:
 
1. Push this repo to GitHub
2. Import the project into Vercel
3. Add `MONGODB_URI` under **Settings → Environment Variables**
4. Deploy 🚀
