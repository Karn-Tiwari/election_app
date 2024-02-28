###Election Application
##Overview
This backend application serves as a voting system where users can cast their votes for candidates. It provides functionalities for user authentication, candidate management, and voting operations. The application is built using Node.js, Express.js, MongoDB, and employs JSON Web Tokens (JWT) for user authentication.

##Features
User Authentication: Users can sign up and log in using their Aadhar Card Number and password.
Candidate Management: Admin users can manage candidates, including adding, updating, and deleting candidate information.
Voting: Users can vote for their preferred candidate. Each user can vote only once.
Vote Count: The application provides endpoints to retrieve the count of votes for each candidate.
User Profile: Users can view their profile information and change their passwords.
##Technologies Used
Node.js: A JavaScript runtime environment for building server-side applications.
Express.js: A web application framework for Node.js that simplifies building APIs.
MongoDB: A NoSQL database used for storing candidate and user information.
JSON Web Tokens (JWT): A standard for securely transmitting information between parties, used for user authentication.
#API Endpoints
#Authentication
#Sign Up
POST /signup: Registers a new user with Aadhar Card Number and password.
#Login
POST /login: Authenticates a user and returns a JWT token for subsequent requests.
##Candidates
#Get Candidates
GET /candidates: Retrieves the list of candidates.
#Add Candidate
POST /candidates: Adds a new candidate to the database. (Admin only)
#Update Candidate
PUT /candidates/:id: Updates candidate information by ID. (Admin only)
#Delete Candidate
DELETE /candidates/:id: Deletes a candidate by ID. (Admin only)
##Voting
#Get Vote Count
GET /candidates/vote/count: Retrieves the count of votes for each candidate.
#Vote for Candidate
POST /candidates/vote/:id: Casts a vote for a candidate. (User only)
##User Profile
#Get Profile
GET /users/profile: Retrieves user profile information.
#Change Password
PUT /users/profile/password: Updates user password.
