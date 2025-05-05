# Cosmopolliton

## Overview

Cosmopolliton is a full-stack web application designed to create, vote on, and analyze polls. It provides an interactive and user-friendly platform for users to manage polls, cast votes, and view results in both textual and graphical formats.

## Features

- **User Authentication**: Secure registration and login system.
- **Poll Creation**: Users can create polls with multiple topics for voting.
- **Voting System**: Users can vote on polls with a limited number of votes per topic.
- **Results Visualization**: Poll results are displayed as rankings and interactive graphs.
- **Past Polls Access**: Users can review and analyze their previously created polls.
- **Guest Voting**: Allows users to vote on polls without logging in.
- **Interactive Dashboard**: Centralized interface for managing polls and accessing features.

## Technologies Used

### Frontend

- **React.js**: For building the user interface.
- **React Router**: For navigation between pages.
- **Plotly.js**: For visualizing poll results.

### Backend

- **Node.js & Express.js**: For server-side logic and API endpoints.
- **MongoDB & Mongoose**: For database management.
- **JWT & bcrypt.js**: For secure authentication and password encryption.

## Testing

### Frontend Testing

- **Jest**: Used for unit testing React components.
- **React Testing Library**: Ensures components behave as expected in various scenarios.
- **End-to-End Testing**: Simulates user interactions to verify the app's functionality.

Tests cover:

- Component rendering and behavior.
- Form validation and submission.
- Navigation between pages.
- Poll creation, voting, and results visualization.

Run tests with the following command:

```bash
cd client
npm test
```

## Project Structure

```
/ - Root Directory
  ├── client/ - Frontend Code
  │   ├── tests/
  │   │   ├── Dashboard.test.js
  │   │   ├── PastPolls.testsjs
  │   │   ├── Register.tests.js
  │   ├── src/
  │   │   ├── pages/
  │   │   │   ├── Confirmation.jsx
  │   │   │   ├── CreatePoll.jsx
  │   │   │   ├── Dashboard.jsx
  │   │   │   ├── HomePage.css
  │   │   │   ├── HomePage.jsx
  │   │   │   ├── Login-Page.css
  │   │   │   ├── Login-Page.jsx
  │   │   │   ├── nav.css
  │   │   │   ├── NavBar.jsx
  │   │   │   ├── PastPills-Graph.jsx
  │   │   │   ├── PastPoll.jsx
  │   │   │   ├── Register.css
  │   │   │   ├── Refister.jsx
  │   │   │   ├── Results-Graph.jsx
  │   │   │   ├── Results.jsx
  │   │   │   ├── Style.css
  │   │   │   ├── VotingPage.jsx
  │   │   ├── App.css
  │   │   ├── App.jsx
  │   │   ├── index.css
  │   │   ├── main.jsx
  │   ├── .gitignore
  │   ├── bable.config.js
  │   ├── eslint.config.js
  │   ├── package.json - Dependencies and scripts
  │   ├── setupTests.js
  │   ├── vite.config.js
  ├── server/ - Backend Code
  │   ├── controllers/
  │   │   ├── authenticationController.js
  │   │   ├── pollController.js
  │   ├── models/
  │   │   ├── users.js
  │   ├── routers/
  │   │   ├── routers.js
  │   ├── server.js - Main backend entry point
  ├── [README.md](http://_vscodecontentref_/0) - Documentation
```

## API Endpoints

## Authentication

- POST /user/login - Authenticates a user.
- POST /user/register - Registers a new user.

## Poll Management

- `POST /user/create-poll` - Creates a new poll.
- `GET /user/pastpolls/:username` - Retrieves past polls created by a user.
- `GET /user/voting-page/:code` - Fetches poll details for voting.
- `PATCH /user/updated-votes` - Updates poll votes.
- `GET /user/results/:code` - Retrieves results of a specific poll.

## User Flow

1. **User Registration & Login**

- New users register with a username and password.
- Existing users log in to access their dashboard.

2. **Dashboard Management**

- Users can create a new poll or enter a poll code to vote.
- Users can view past polls and analyze previous results.

3. **Creating a Poll**

- Users define a poll name and add multiple topics for voting.
- Polls are assigned a unique code for sharing.

4. **Voting Process**

- Users enter a poll code to participate.
- Votes are submitted and updated in the database.

5. **Viewing Results**

- Users can view rankings or graphical representations of poll results.
- Results are accessible immediately after voting.

## Security Considerations

- **Password Hashing**: User passwords are securely hashed using bcrypt.js.
- **JWT Authentication**: Ensures secure user sessions.
- **Input Validation**: Prevents unauthorized or invalid data submissions.

## How to Use

- Clone the repository and navigate to the project directory.
- Install dependencies for both the client and server:
- Start the backend server:
- Start the frontend development server:
- Open the application in your browser at http://localhost:5173.

## Contributors

Developed by the Goblin Sharks, iterated on by the Dangerous-Noodle-Cosmo .

## License

This project is licensed under the MIT License. ```
