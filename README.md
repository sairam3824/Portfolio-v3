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

### Custom domain setup (`saiii.in`)

Keep hostname redirects in one place only. Do not configure `saiii.in -> www.saiii.in`
in your DNS provider or Cloudflare while the app is also redirecting `www -> apex`, or
you will create a redirect loop.

Recommended setup for this project:

1. Add both `saiii.in` and `www.saiii.in` to the same Vercel project.
2. Connect `saiii.in` to `Production`.
3. Set `www.saiii.in` to `Redirect to Another Domain` -> `saiii.in`.
4. Remove any registrar or Cloudflare forwarding rule that redirects `saiii.in` to
   `www.saiii.in`.

DNS should point to Vercel instead of doing URL forwarding:

- Apex `saiii.in`: `A` record to `76.76.21.21`
- `www.saiii.in`: `CNAME` to the target shown by Vercel for your project
 
