🌍 Overview
LevKonnect is a platform that connects engineers, technicians, and energy professionals with clients looking for services, focusing on clean and sustainable energy solutions across Tanzania and Africa.

🔹 Mission
Empowering sustainable energy access in Africa by bridging the gap between skilled professionals and clients.

🚀 Key Features
Job Posting & Bidding – Clients post jobs, engineers bid on them.

Project Management – Track progress, manage milestones, and ensure successful project delivery.

Communication Hub – Real-time messaging and notifications for seamless collaboration.

📌 Features
🔹 Functional Requirements
🛠 User Registration & Authentication
✔ Register as a Client or Engineer
✔ Email Verification using OAuth 2.0 or JWT
✔ Password Recovery via secure reset link
✔ Role-Based Access – Redirect users to their respective dashboards
✔ Logout securely clears session

📋 Job Posting & Bidding
✔ Clients post jobs with budget, timeline, and required skills
✔ Engineers bid on jobs with amount, duration, and cover letter
✔ Search & Filter jobs by category, location, budget, and skills
✔ Clients accept bids, marking jobs as "in-progress"

📊 Project Management
✔ View project overview, status, and deliverables
✔ Create & Track Milestones – Clients create milestones, engineers mark them as completed

💬 Communication Hub
✔ Messaging System – Project-specific chat between clients and engineers
✔ Real-time Notifications – Updates on messages, bids, milestones, and project changes

🔧 Admin Management
✔ User Management – Suspend or delete user accounts
✔ Moderate Job Postings – Approve or reject job listings
✔ Platform Metrics – Track number of users, jobs, and completed projects

⚙️ Technologies Used
🖥 Backend
Language: JavaScript (Node.js)

Framework: Express.js

Database: MySQL 5.5.62

Libraries:

bcrypt & bcryptjs (password hashing)

cors (CORS policy handling)

dotenv (environment variables)

express-validator (input validation)

jsonwebtoken (JWT authentication)

morgan (HTTP request logging)

mysql2 (MySQL client)

nodemailer (email services)

sequelize (ORM for MySQL)

🌐 Frontend
Languages: JavaScript / TypeScript, HTML, CSS

Framework: React (Vite as the build tool)

Libraries:

@tailwindcss/vite (Tailwind CSS)

axios (API requests)

firebase (Authentication)

lucide-react & react-icons (Icons)

react-router-dom (Client-side routing)

🛠 Additional Tools
Package Manager: npm

Testing & Debugging: Postman, Browser DevTools

🏗 Setup & Installation
✅ Prerequisites
Before running LevKonnect, ensure you have:
✔ Node.js (v16+)
✔ npm (v8+)
✔ MySQL (v5.5+, recommended v8.0)
✔ Git
✔ Gmail Account (for email notifications via Nodemailer)
✔ Firebase Account (if authentication is handled via Firebase)

🚀 Installation Steps
1️⃣ Clone the Repository

git clone https://github.com/ramadhaniwanjenja/LevKonnect.git
cd LevKonnect
2️⃣ Setup the Backend

cd backend
npm install
🛠 Configure Backend Environment Variables
Create a .env file in the backend/ directory and add:

# Database Configuration
DB_HOST=sql12.freesqldatabase.com
DB_USER=your_db_user
DB_PASSWORD=your_db_password
DB_NAME=your_db_name
DB_PORT=3306

# Email Configuration (Nodemailer)
EMAIL_HOST=smtp.gmail.com
EMAIL_PORT=587
EMAIL_USER=your-email@gmail.com
EMAIL_PASS=your-app-password
SUPPORT_EMAIL=your-support-email@gmail.com

# JWT Configuration
JWT_SECRET=your_jwt_secret

# Server Configuration
PORT=5000
🛠 Setup the Database
Ensure MySQL is running

Create the database manually:


CREATE DATABASE your_db_name;
✅ Sequelize will automatically create tables on server startup

🔧 Run the Backend

npm run dev
Backend runs on: http://localhost:5000

3️⃣ Setup the Frontend

cd ../frontend
npm install
🔧 Run the Frontend

npm run dev
Frontend runs on: http://localhost:5173

🚀 Production Build & Deployment
🛠 Backend
No build step required, just run:


cd backend
node server.js
🖥 Frontend
Build and serve the frontend for production:


cd frontend
npm run build
npm run preview
🚀 Deployment
Platform	Service Used
Frontend	Vercel
Backend	Render
Database	DigitalOcean MySQL / AWS RDS
Deployment Steps
✔ Add .env variables to the deployment platform
✔ Connect GitHub Repo to the deployment service
✔ Configure Build Settings

Frontend: npm run build → Output: dist/

Backend: node server.js
✔ Deploy Frontend & Backend
✔ Update VITE_API_URL in frontend to match the deployed backend

🤝 Contributing
💡 Contribution Workflow
Fork the repository

Create a feature branch:

bash
Copy
Edit
git checkout -b feature/AmazingFeature
Commit changes:

bash
Copy
Edit
git commit -m "Add some AmazingFeature"
Push to GitHub:

bash
Copy
Edit
git push origin feature/AmazingFeature
Open a Pull Request (PR)

📌 Code Style Guidelines
✔ ESLint: Run npm run lint
✔ Prettier: Run npm run format
✔ Follow modular coding best practices
✔ Add comments for complex logic
✔ Ensure all features are tested

📞 Contact
✉️ LevKonnect Dev Team at ALU
📧 Email: r.wanjenja@alustudent.com
🔗 Project Link: LevKonnect on GitHub
