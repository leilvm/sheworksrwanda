# sheworksrwanda
SheWorks Rwanda

Overview

SheWorks is an innovative platform aimed at bridging the gap between education and employment for women in Rwanda through the tourism sector. The platform helps connect women job seekers with employment opportunities in tourism and related industries. This project was built with the intention of leveraging technology to empower women in Rwanda and contribute to the country's economic growth through sustainable tourism.

How the App Was Created
1. Project Setup
The project was initially set up using create-react-app to quickly set up a React-based frontend. The following steps were taken to configure the application:

Create React App: I used the create-react-app command to initialize the project.

bash
Copy
Edit
npx create-react-app user-app
Folder Structure: The basic folder structure was configured with separate folders for components, assets, and services.

bash
Copy
Edit
/src
   /components
   /assets
   /services
2. Frontend Development
The frontend was developed using React to create a responsive and user-friendly interface. Key features include:

Landing Page: The landing page was designed to introduce SheWorks and its mission. This includes sections such as testimonials, a list of partners, and a newsletter signup form.

React Router: React Router was used for navigation within the app, including pages for job listings, user registration, and contact forms.

To set up React Router:

bash
Copy
Edit
npm install react-router-dom
State Management: State management was handled using React's built-in state hooks (useState and useEffect). This is used for managing form data, fetching job listings, and handling user interactions.

3. Backend (API Integration)
For the backend, I integrated APIs that would serve data related to tourism job listings and user registrations:

Node.js and Express: The backend was set up using Node.js with the Express framework. This was used to handle API routes for fetching job data, handling user input, and submitting forms.

MongoDB: MongoDB was used for data storage, where job listings, user details, and applications are saved.

APIs for Job Listings: I created APIs that fetch job listings from tourism-related companies and integrate them into the frontend.

Example API route:

js
Copy
Edit
app.get('/api/jobs', (req, res) => {
  Job.find({}, (err, jobs) => {
    if (err) {
      res.status(500).send('Error retrieving job listings');
    }
    res.json(jobs);
  });
});
4. Deployment
Frontend Deployment: The React app was deployed on Vercel to ensure it is accessible globally. For the frontend, I used Vercel's integration with GitHub for Continuous Deployment.

Steps to deploy on Vercel:

Push the code to a GitHub repository.

Connect the GitHub repository to Vercel through the Vercel dashboard.

Configure the deployment settings (set the build command to npm run build and output directory to build).

Backend Deployment: The backend was deployed using Heroku. I set up the environment, installed necessary dependencies (express, mongoose, etc.), and configured the app for production deployment.

Heroku Deployment: After setting up the backend, the app was deployed using Heroku’s Git integration:

bash
Copy
Edit
git push heroku master
Domain Name: For the production environment, I set up a custom domain (sheworks-one.vercel.app) through Vercel to make the app accessible via a real URL.

Configured the "homepage" field in package.json to the Vercel URL.

Example:

json
Copy
Edit
"homepage": "https://sheworks-one.vercel.app"
5. Ethical Considerations
The app was designed with ethical considerations in mind, focusing on the empowerment of women and the promotion of inclusive employment opportunities. Some key considerations:

Data Privacy: Ensured that users' personal data is handled securely, following best practices for storing and managing sensitive information.

Inclusivity: The app was developed with inclusivity in mind, ensuring that women from various socio-economic backgrounds could access the platform.

Sustainability: The use of tourism as a key sector was chosen for its potential to contribute to sustainable economic development, providing long-term employment opportunities in the region.

6. Technologies Used
Frontend:

React.js

React Router

CSS3 and HTML5

Axios (for API requests)

Backend:

Node.js

Express.js

MongoDB (database)

Deployment:

Vercel (for frontend deployment)

Heroku (for backend deployment)

7. Challenges and Lessons Learned
Integration of APIs: One of the biggest challenges was integrating the frontend with the backend APIs, especially in ensuring the data flow was smooth and consistent across both.

Routing Issues: Handling client-side routing on Vercel required some additional configuration to ensure that React Router worked properly with the static deployment.

Security: Implementing secure data management and user authentication was another challenge, but it was crucial for maintaining user privacy and trust.

8. Future Work
User Authentication: I plan to add user authentication (sign-up/sign-in functionality) using JWT tokens to secure access to the platform.

Job Application Process: Implementing the ability for users to apply directly to job listings through the app, with email notifications sent to employers.

Expand Job Listings: I intend to expand the job listings by collaborating with more tourism businesses in Rwanda.

Getting Started
To run the app locally, follow these steps:

Clone the repository:

bash
Copy
Edit
git clone https://github.com/leilvm/sheworks.git
Install the required dependencies:

bash
Copy
Edit
cd user-app
npm install
Start the development server:

bash
Copy
Edit
npm start
The app will be available at http://localhost:3000.

