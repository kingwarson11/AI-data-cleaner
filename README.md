# AI Data Cleaning Studio

Paste dirty data → Claude AI predicts every issue → get pristine matched tables with full before/after comparison and a clean SQL schema.

## Features
- AI-predicted cleaning operations (case, emails, phones, dates, currencies, duplicates, nulls, negatives, and more)
- Side-by-side before/after table comparison with highlighted diffs
- Matched, normalized schema with inferred types
- Auto-generated SQL `CREATE TABLE` statement
- Download clean CSV
- Four built-in sample dirty datasets

## Local development

```bash
npm install
cp .env.example .env        # add your ANTHROPIC_API_KEY
npm run dev                  # runs on http://localhost:3000
```

## Deploy to GitHub

```bash
git init
git add .
git commit -m "initial commit"
gh repo create ai-data-cleaner --public --push --source=.
# or: git remote add origin https://github.com/YOUR_USERNAME/ai-data-cleaner.git && git push -u origin main
```

## Deploy to Vercel (recommended — fastest)

```bash
npm i -g vercel
vercel
# follow prompts, then:
vercel env add ANTHROPIC_API_KEY   # paste your key when prompted
vercel --prod
```

Or connect via Vercel dashboard:
1. Import your GitHub repo at vercel.com/new
2. Add `ANTHROPIC_API_KEY` under Settings → Environment Variables
3. Deploy

## Deploy to Render

1. Push to GitHub (see above)
2. Go to render.com → New → Web Service
3. Connect your GitHub repo
4. Settings:
   - **Environment**: Node
   - **Build command**: `npm install`
   - **Start command**: `npm start`
5. Add environment variable: `ANTHROPIC_API_KEY` = your key
6. Click Deploy

## Environment variables

| Variable | Required | Description |
|---|---|---|
| `ANTHROPIC_API_KEY` | Yes | Your Anthropic API key from console.anthropic.com |
| `PORT` | No | Port to listen on (default: 3000, auto-set by Render/Vercel) |
# AI-data-cleaner
# AI-data-cleaner
