# Portfolio v3

Production portfolio built with Vite, React, Tailwind, Supabase, and a Vercel serverless chat endpoint.

## Setup

1. Install dependencies:
   `npm install`
2. Create an env file:
   `cp .env.example .env.local`
3. Fill in the required values:
   - `VITE_SUPABASE_URL`
   - `VITE_SUPABASE_ANON_KEY`
   - `OPENAI_API_KEY`

## Local Development

- `npm run dev`
  Runs the frontend with Vite.
- `vercel dev`
  Runs the Vite app together with `/api/chat` so the chat widget works locally.

## Quality Checks

- `npm run lint`
- `npm run build`

## Deployment

Deploy to Vercel with the same environment variables configured in the project settings.
