# RailOps Enterprise DBMS

RailOps Enterprise DBMS is a full-stack Railway Database Management System built with Flask, MySQL, Bootstrap 5, HTML5, CSS3, JavaScript, and Font Awesome. It provides an enterprise-style administrator dashboard for managing railway trains, stations, routes, schedules, employees, and reports from one centralized web application.


## Key Features

- Secure admin login and session management
- Professional railway dashboard interface
- Live IST clock and current date display
- Dynamic database statistics
- Train, station, route, schedule, and employee management
- Full CRUD operations with modal forms
- Search, sorting, pagination, and validation
- Toast notifications for user actions
- Latest records table on dashboard
- Report generation for trains, stations, routes, and employees
- Export support for PDF, Excel, and CSV
- Responsive Bootstrap 5 layout
- Vercel deployment support

## Modules

### Dashboard

- Railway-themed hero banner
- System information panel
- Total trains, stations, routes, and employees
- Quick access actions
- Latest records overview

### Train Management

- Add, edit, delete, and search trains
- Manage train number, name, source, destination, and capacity

### Station Management

- Add, edit, delete, and search stations
- Manage station code, station name, city, state, and platform count

### Route Management

- Add, edit, delete, and search routes
- Manage source station, destination station, and route distance

### Schedule Management

- Assign trains to routes
- Manage arrival time, departure time, and platform number

### Employee Management

- Add, update, delete, and search employees
- Manage employee role, department, contact details, and status

### Reports

- Generate train, station, route, and employee reports
- Export reports as PDF, Excel, or CSV

## Tech Stack

- Python Flask
- Flask-SQLAlchemy
- MySQL
- SQLite fallback for local/demo use
- HTML5
- CSS3
- JavaScript
- Bootstrap 5
- Font Awesome Icons
- Vercel Serverless Functions

## Project Structure

```text
railway-dbms/
├── api/
│   └── index.py
├── public/
│   ├── app.js
│   ├── railway-hero.png
│   └── style.css
├── static/
│   ├── css/
│   ├── img/
│   └── js/
├── templates/
│   ├── base.html
│   ├── dashboard.html
│   ├── login.html
│   ├── crud.html
│   ├── schedules.html
│   ├── reports.html
│   └── settings.html
├── app.py
├── run.py
├── schema.sql
├── requirements.txt
├── vercel.json
├── Procfile
└── README.md
```


## Author

Developed by Shambhavi.

## License

This project is licensed under the MIT License.
