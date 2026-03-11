# Budget Flow

Budget tracker with MySQL-backed authentication, category management, charts, and monthly summaries.

## Project Structure

```
Budget/
  public/
    index.html
    styles.css
    js/
      app.js
  src/
    server.js
    config/
      db.js
    routes/
      auth.routes.js
    middleware/
      errorHandler.js
  sql/
    init.sql
  .env.example
  .gitignore
  package.json
```

## Features

- Username/password authentication with MySQL storage
- Password hashing with `bcryptjs`
- Monthly expense tracking and recurring expenses
- Category management with search and alphabetical ordering
- Dashboard summary cards and charts
- Category totals table sorted by amount

## Setup

1. Install dependencies:
   `npm install`
2. Create a local env file from template:
   `copy .env.example .env`
3. Edit `.env` with your MySQL credentials.
4. Ensure database/table exist (example in `sql/init.sql`).
5. Start app:
   `npm start`
6. Open:
   `http://localhost:3000`

## API Endpoints

- `POST /register`
- `POST /login`
- `GET /health`

## Security Notes

- Secrets are read from `.env`.
- `.env` is ignored by git via `.gitignore`.
- Do not commit real passwords or production credentials.
