# LevKonnect
***
## Overview
LevKonnect is a powerful platform designed to connect engineers, technicians, and energy professionals with clients seeking their services, with a focus on promoting clean and sustainable energy solutions in Tanzania and across Africa. Whether you’re a client looking to post a job or an engineer seeking opportunities, LevKonnect streamlines the process with intuitive dashboards, job bidding, project management, and for low-bandwidth environments and mobile-first usage.

***
🌍 Mission: Empower sustainable energy access in Africa by bridging the gap between skilled professionals and clients.

***
🚀 Key Features: Job posting, bidding, project management, and a communication hub for seamless collaboration.

### Features
LevKonnect offers a wide range of features to ensure a smooth experience for clients, engineers, and admins. Below are the functional and non-functional requirements that define the platform’s capabilities.

### Functional Requirements
**User Registration and Authentication**		
1. Register as a new member	Users can register as clients or engineers using their email address.
2. Verify your account	Email verification link sent to authenticate users using OAuth 2.0 or JWT.
3. Password recovery	Users can recover their password via a secure reset link sent to their email
4. Login with role-based access	Users log in and are redirected to their respective dashboards (client, engineer, admin).	High
5. Logout functionality	Users can log out, securely clearing their session.	Medium

**Job Posting and Bidding**		
1. Post job	Clients can post jobs with details like project description, budget, timeline, and skills.
2. Bid on relevant job	Engineers can bid on jobs with a bid amount, delivery days, and cover letter.
3. Search and filter jobs	Engineers can search and filter jobs by category, location, budget, and skills.
4. View job details	Users can view detailed job info, including client details and bids.
5. Accept a bid	Clients can accept a bid, marking the job as "in-progress" and notifying the engineer.

**Project Management**		
1. View project overview	Users can view active project details, including status, timeline, and deliverables.
2. Create and track milestones	Clients can create milestones, and engineers can mark them as completed. 

**Communication Hub**		
1. Send and receive messages	Clients and engineers can message each other within a project-specific chat.
2. Receive notifications	Users get notified of messages, bid updates, milestone approvals, and project changes.

**Admin Management**		
1. Manage users	Admins can view, suspend, or delete user accounts.
2. Moderate job postings	Admins can review and approve/reject job postings for compliance.
3. View platform metrics	Admins can view metrics (e.g., number of users, jobs posted, completed projects).

***

## Technologies Used
LevKonnect is built with a modern tech stack to ensure performance, scalability, and a great user experience.

**Backend**
*Language:* JavaScript (Node.js, CommonJS)
*Framework:* Express

*Libraries:*
1. 'bcrypt & bcryptjs': Password hashing
2. 'cors': Cross-Origin Resource Sharing
3. 'dotenv': Environment variable management
4. 'express-validator': Input validation
5. 'jsonwebtoken': JWT authentication
6. 'morgan': HTTP request logging
7. 'mysql2': MySQL client
8. 'nodemailer': Email sending
9. 'sequelize': ORM for MySQL
10. Dev Tools: 'nodemon'
11. Database: 'MySQL 5.5.62'

**Frontend**

*Languages:* JavaScript/TypeScript, HTML, CSS
*Framework:* React (with Vite as the build tool)

*Libraries:*
1. @tailwindcss/vite: Tailwind CSS integration
2. axios: HTTP requests
3. firebase: Authentication and Firebase services
4. lucide-react: Icons
5. react-icons: Additional icons
6. react-router-dom: Client-side routing
7. Build Tool: Vite


**Additional Tools**

*Package Manager:* 'npm'
*Testing/Debugging:* Postman, Browser DevTools 

***

## Prerequisites
Before setting up LevKonnect, ensure you have the following installed:

- 'Node.js' (v16 or higher)
- 'npm' (v8 or higher)
- 'MySQL' (v5.5 or higher; recommend v8.0 for better performance)
- Git
- Gmail Account (for Nodemailer email notifications)
- Firebase Account (for authentication, if used)
- Environment Setup
- Follow these steps to get LevKonnect up and running on your local machine. The project has two - parts: *the backend and the frontend.*

1. **Clone the Repository**
```bash
'git clone https://github.com/ramadhaniwanjenja/LevKonnect.git'
'cd LevKonnect'

2. **Set Up the Backend**
```bash
cd backend

### Install Backend Dependencies
```bash
npm install

### Configure Backend Environment Variables
Create a '.env' file in the 'backend/' directory with the following variables:

```bash
# Database Configuration
DB_HOST=sql12.freesqldatabase.com
DB_USER=your_db_user
DB_PASSWORD=your_db_password
DB_NAME=your_db_name
DB_PORT=3306

# Email Configuration (for Nodemailer)
EMAIL_HOST=smtp.gmail.com
EMAIL_PORT=587
EMAIL_USER=your-email@gmail.com
EMAIL_PASS=your-app-password
SUPPORT_EMAIL=your-support-email@gmail.com

# JWT Configuration
JWT_SECRET=your_jwt_secret

### Server Configuration
PORT=5000
Database: Replace DB_HOST, DB_USER, DB_PASSWORD, and DB_NAME with your MySQL database credentials.
Email: Replace EMAIL_USER with your Gmail address and EMAIL_PASS with a Gmail App Password (generate one from your Google Account settings).
JWT: Replace JWT_SECRET with a secure random string for JWT authentication.

***

## Set Up the Database
1. Ensure your MySQL server is running.
2. Create the database (if not already created):

```sql
CREATE DATABASE your_db_name;

3. Sequelize will automatically create the tables when you start the server (thanks to sync in db.config.js).

**Run the Backend**
```bash
npm run dev

The backend will start on http://localhost:5000.

3. **Set Up the Frontend**
Navigate to the Frontend Directory

```bash
cd ../frontend

**Install Frontend Dependencies**
```bash

npm install


**Run the Frontend**
```bash
npm run dev

- The frontend will start on http://localhost:5173.
- Visit http://localhost:5173/ in your browser (it will redirect to /home).


## Production Build
**Backend**
The backend doesn’t require a build step (it’s Node.js). Just run:

```bash
cd backend
node server.js

**Frontend**
Build and serve the frontend for production:

```bash
cd frontend
npm run build
npm run preview



## Deployment
***
### Deployment Platforms
1. **Frontend:** Vercel
2. **Backend:** Render
3. **Database:** Use a managed MySQL service like DigitalOcean MySQL or AWS RDS.


## Deployment Steps
1. Set Up Environment Variables:
2. Add the .env variables to your deployment platform’s environment settings.
3. Connect Your GitHub Repository:
4. Link your GitHub repo to the deployment platform.
5. Configure Build Settings:
6. Frontend: Set the build command to npm run build and the output directory to dist.
7. Backend: Set the start command to node server.js.
8. Deploy:
9. Deploy the frontend and backend separately.
10. Update VITE_API_URL in the frontend to point to the deployed backend URL.

## Contributing
***
We welcome contributions to LevKonnect! Follow these steps to contribute:

## Development Workflow
1. Fork the repository.
2. Create a feature branch:
```bash
git checkout -b feature/AmazingFeature
3. Commit your changes:
```bash
git commit -m 'Add some AmazingFeature'
4. Push to the branch:
```bash
git push origin feature/AmazingFeature
5. Open a Pull Request on GitHub.


## Code Style
- *ESLint:* Run npm run lint to check for linting errors.
- *Prettier:* Run npm run format to format your code.
- *Guidelines:*
- Follow modular coding practices.
- Add comments for complex logic.
- Ensure all new features are tested.
***

Contact
LevKonnect Dev Team at ALU
- Email: r.wanjenja@alustudent.com
- Project Link: https://github.com/ramadhaniwanjenja/LevKonnect.git
