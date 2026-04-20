
# Incident Reporting System

## 📦 Installation

```bash
npm install
```

## ⚙️ Setup Environment Variables

Create a `.env.local` file and fill:

```
NEXT_PUBLIC_SUPABASE_URL=your_url
NEXT_PUBLIC_SUPABASE_ANON_KEY=your_key
OPENAI_API_KEY=your_key
```

## 🗄️ Database Setup

Go to Supabase SQL Editor and run:

```sql
create table incidents (
  id uuid default gen_random_uuid() primary key,
  raw_text text,
  summary text,
  type text,
  emotion_score int,
  priority text,
  status text default 'New',
  assigned_team text,
  report_markdown text,
  created_at timestamp default now()
);
```

## ▶️ Run

```bash
npm run dev
```

Open:

http://localhost:3000

```
```
