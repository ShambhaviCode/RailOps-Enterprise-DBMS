# Railway Database Management System

Professional Flask + MySQL railway management dashboard with authentication, live IST clock, CRUD modules, dynamic statistics, search, sorting, pagination, modal forms, toast notifications, and report exports.

## Login

- Username: `admin`
- Password: `admin123`

## Run Locally

```powershell
cd C:\Users\Shambhavi\Documents\Codex\2026-06-13\build-a-railway-database-management-system\outputs\railway-dbms
python -m venv .venv
.\.venv\Scripts\Activate.ps1
pip install -r requirements.txt
python app.py
```

Open `http://127.0.0.1:5000`.

## MySQL Setup

Create the database with:

```powershell
mysql -u root -p < schema.sql
```

Then run the app with MySQL:

```powershell
$env:DB_ENGINE="mysql"
$env:MYSQL_HOST="localhost"
$env:MYSQL_PORT="3306"
$env:MYSQL_DATABASE="railway_dbms"
$env:MYSQL_USER="root"
$env:MYSQL_PASSWORD="your_password"
python app.py
```

If `DB_ENGINE` is not set, the app uses a local SQLite database in `instance/railway_dbms.sqlite` so the dashboard can be tested immediately.

## Deploy

Use a Python web host such as Render, Railway, PythonAnywhere, or a VPS.

Production start command:

```bash
gunicorn app:app
```

Set these environment variables on the host:

```text
SECRET_KEY=change-this-to-a-long-random-secret
DB_ENGINE=mysql
MYSQL_HOST=your-mysql-host
MYSQL_PORT=3306
MYSQL_DATABASE=railway_dbms
MYSQL_USER=your-mysql-user
MYSQL_PASSWORD=your-mysql-password
```

Import `schema.sql` into your hosted MySQL database before opening the deployed site.

## Deploy on Vercel

Vercel runs this Flask app as a serverless Python function through `api/index.py`.

1. Push the `railway-dbms` folder to GitHub.
2. Create an external MySQL database. Do not use SQLite on Vercel.
3. Import `schema.sql` into the MySQL database.
4. In Vercel, create a new project from the GitHub repository.
5. If your repo contains other folders, set the Vercel root directory to `outputs/railway-dbms`.
6. Add these Vercel Environment Variables:

```text
SECRET_KEY=change-this-to-a-long-random-secret
DB_ENGINE=mysql
MYSQL_HOST=your-mysql-host
MYSQL_PORT=3306
MYSQL_DATABASE=railway_dbms
MYSQL_USER=your-mysql-user
MYSQL_PASSWORD=your-mysql-password
```

7. Deploy. Vercel will install `requirements.txt` and use `vercel.json`.

The Vercel entrypoint is `api/index.py`.

## Included Modules

- Dashboard with railway banner, system information, live statistics, quick access, and latest records
- Train Management
- Station Management
- Route Management
- Schedule Management
- Employee Management
- Report Generation with PDF, Excel, and CSV exports
- System Settings
