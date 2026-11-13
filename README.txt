# Dixitgram Online Starter

This is a starter project, not a live website yet. It requires a Supabase project and a hosting account to publish.

## What it includes
- Email/password sign-up and login
- Google OAuth button (works only after Google provider setup)
- Phone OTP flow (requires an SMS provider; SMS may cost money)
- Signed-in-only video feed
- Authenticated video uploads to a private bucket
- Likes, comments, and a basic report button
- Row Level Security policies

## Setup (ask a parent/guardian to help with public launch)
1. Create a Supabase project.
2. In Supabase SQL Editor, run `supabase_setup.sql`.
3. In Storage, create a **private** bucket named `videos`. Set a sensible upload limit and allowed MIME types.
4. In Authentication > Providers, enable Email. Configure Google OAuth credentials to enable Google login.
5. For phone OTP, configure an SMS provider and follow applicable local requirements. SMS is not automatically free.
6. Open `index.html` and replace:
   - `PASTE_YOUR_SUPABASE_PROJECT_URL`
   - `PASTE_YOUR_SUPABASE_PUBLISHABLE_OR_ANON_KEY`
   with the Project URL and publishable/anon key from Project Settings > API.
   **Never put a service_role/secret key in this website.**
7. Publish the folder using a static website host such as Vercel. Add the deployed site URL to Supabase Auth redirect URLs.

## Important safety and launch limitations
- This is a learning starter, not production-ready social media software.
- A public user-generated-video service needs active moderation, report review, blocking, rate limits, abuse prevention, privacy policy, terms, age-appropriate safeguards, and a process for removing harmful/unauthorized content before inviting the public.
- The sample report button stores reports; it does not automatically review or remove reported videos.
- Add profile management, follow system, comment moderation, admin tools, video transcoding, quotas, backups, and stronger abuse controls before public launch.
- Do not share passwords, OTPs, secret keys, or account recovery codes in chat.
- Ask a parent/guardian to supervise accounts, billing, publishing, and privacy/legal decisions.
