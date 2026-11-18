# Lizzy AI — starter website

A responsive Next.js AI chat app with Supabase email/password accounts, per-user private chat history, and a server-side OpenAI API route.

## Requirements
- Node.js 20.9+
- Supabase project
- OpenAI API key (API billing may apply)

## Setup
1. Run `npm install`.
2. Create a project at https://supabase.com/.
3. In Supabase Project Settings → API, copy the Project URL and anon/public key.
4. Open Supabase SQL Editor and run `supabase/schema.sql`.
5. In Supabase Authentication settings, enable Email sign-in.
6. Copy `.env.example` to `.env.local` and fill in the Supabase URL, Supabase anon key, and OpenAI API key.
7. Get your API key at https://platform.openai.com/api-keys. Keep it secret; do not add `NEXT_PUBLIC_` to its variable name.
8. Run `npm run dev`, then open http://localhost:3000.

Create one account for yourself and another for your girlfriend. Each account has private chats; this initial version does not expose one person's private conversations to the other. A shared couple space can be added later with explicit sharing controls.

## Deploy
Push to a private GitHub repository, import it into https://vercel.com/, add the three environment variables in Vercel project settings, and deploy. Set the Supabase Auth Site URL and allowed redirect URL to your deployed domain.

## Before public launch
Add rate limiting, abuse monitoring, a privacy policy, and any required data-retention controls. Do not store highly sensitive personal information. API use may incur charges; configure usage limits in your OpenAI account.
