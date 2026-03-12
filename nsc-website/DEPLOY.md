# No Sleep Club — Deployment Guide

## Quick Deploy to Vercel

### Option 1: Vercel CLI (fastest)
```bash
cd nsc-website
npx vercel --prod
```
Follow the prompts — it'll ask you to log in and link/create a project.

### Option 2: GitHub + Vercel (auto-deploys)
1. Create a repo: `git init && git add . && git commit -m "NSC website v1"`
2. Push to GitHub
3. Go to vercel.com → New Project → Import your repo
4. Deploy — done. Every push auto-deploys.

### Option 3: Drag & Drop
1. Go to vercel.com/new
2. Drag the entire `nsc-website` folder into the upload area
3. Click Deploy

## Custom Domain
After deploying, go to your Vercel project → Settings → Domains → Add `nosleepclubto.com`.
Update your DNS:
- **A Record**: `76.76.21.21`
- **CNAME**: `cname.vercel-dns.com`

## Mailchimp Setup
1. Create a free Mailchimp account at mailchimp.com
2. Create an Audience (your mailing list)
3. Go to Audience → Signup Forms → Embedded Forms
4. Copy the form action URL (looks like: `https://nosleepclub.us21.list-manage.com/subscribe/post?u=XXXXX&id=XXXXX`)
5. In `index.html`, find `MAILCHIMP_URL` near the bottom and paste your URL there

## File Structure
```
nsc-website/
├── index.html          # Complete single-page site
├── vercel.json         # Vercel deployment config
├── images/
│   ├── logo.png        # NSC logo
│   ├── shawn-qanun.jpg # LockEight photo
│   ├── massimo-bucci.jpg
│   ├── jared-hines.jpg
│   └── sivan-dubinsky.jpg
└── DEPLOY.md           # This file
```
