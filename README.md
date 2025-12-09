# Mern-Assessment

A complete CRM-style application built using:
Backend: Node.js, Express, MySQL, JWT, BCrypt
Frontend: React (Vite), React Router
No UI Libraries Used (as per requirement)


Features
🔐 Authentication
Register user
Login user
JWT-based authentication
Token stored in localStorage
Auto logout after 15 minutes


Users
View all users (protected route)
Contacts Module
Add contact (unique per user)
List contacts
Validate duplicate numbers
Protected by JWT


Address Module
Select a contact
Add address for that contact
Multiple addresses per contact
List addresses
Ownership validation (cannot access another user’s contacts)


Tasks Module
Select contact
Create task (with title, description, status, due date)
List tasks
Status color badges
Ownership validation
On task creation → email log is created instead of sending email


Email Logs
DB table stores "simulated emails"
Logged when a task is created
No real email sent (as per requirement)


🛠 Backend Setup
1. Go to backend folder
    cd backend
    npm install

2. Create .env
    PORT=4000
    DB_HOST=localhost
    DB_USER=root
    DB_PASSWORD=your_password
    DB_NAME=skillsconnect_db
    JWT_SECRET=your_secret_key

3. Run Backend
    npm run dev


🎨 Frontend Setup
1. Go to frontend folder
    cd frontend
    npm install

2. Run Frontend
    npm run dev


🔗 API Routes (Summary)
Auth
    POST /api/auth/register
    POST /api/auth/login

Users
    GET /api/users

Contacts
    POST /api/contacts
    GET /api/contacts

Address
    POST /api/address
    GET /api/address/:contact_id

Tasks
    POST /api/tasks
    GET /api/tasks


📸 Frontend Pages

1.Login Page
2.Dashboard (fetch users)
3.Contacts Page (list + add)
4.Address Page (select contact → list/add addresses)
5.Tasks Page (select contact → list/create tasks)
All pages protected except Login.
