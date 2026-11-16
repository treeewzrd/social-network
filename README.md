# Social Network API

**Status: Coursework / learning project.**

An Express and MongoDB coursework API for users, thoughts, reactions, and friend relationships.

Preserved as a learning reference; production deployment and current compatibility have not been verified.


![MongoDB](https://img.shields.io/badge/MongoDB-4EA94B?style=for-the-badge&logo=mongodb&logoColor=white)
![Express.js](https://img.shields.io/badge/Express.js-404D59?style=for-the-badge)
![Node.js](https://img.shields.io/badge/Node.js-43853D?style=for-the-badge&logo=node.js&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)

## Description

A robust API for a social network web application where users can share thoughts, react to friends' thoughts, and create a friend list. This application uses Express.js for routing, MongoDB for the database, and Mongoose ODM for data modeling. The API is designed to handle large amounts of unstructured data, making MongoDB an ideal choice for this social network platform.

## Table of Contents

- [Demo](#demo)
- [Installation](#installation)
- [Usage](#usage)
- [API Routes](#api-routes)
  - [User Routes](#user-routes)
  - [Thought Routes](#thought-routes)
  - [Reaction Routes](#reaction-routes)
- [Testing with Insomnia](#testing-with-insomnia)
- [Technologies Used](#technologies-used)
- [License](#license)
- [Credits](#credits)
- [Questions](#questions)

## Demo

Watch the full demonstration of the API functionality:

[View Demo/Video](https://res.cloudinary.com/dswrez3vz/video/upload/v1747988836/SOCIAL_NETWORK_rvnisp.mp4)

## Installation

1. Clone the repository:
```bash
git clone https://github.com/treeewzrd/SOCIAL-NETWORK.git
```

2. Navigate to the project directory:
```bash
cd SOCIAL-NETWORK
```

3. Install dependencies:
```bash
npm install
```

4. Create a `.env` file in the root directory with your MongoDB connection string:
```
MONGODB_URI=mongodb+srv://username:password@cluster.mongodb.net/socialDB?retryWrites=true&w=majority
PORT=3001
```

## Usage

1. Start the server:
```bash
npm start
```

2. The API server will start running on `http://localhost:3001`

3. Use Insomnia or a similar API testing tool to test the various endpoints

## API Routes

### User Routes

- **GET /api/users** - Get all users
- **GET /api/users/:userId** - Get a single user by ID with populated thought and friend data
- **POST /api/users** - Create a new user
  ```json
  {
    "username": "testuser",
    "email": "test@example.com"
  }
  ```
- **PUT /api/users/:userId** - Update a user
- **DELETE /api/users/:userId** - Delete a user (and associated thoughts)
- **POST /api/users/:userId/friends/:friendId** - Add a friend
- **DELETE /api/users/:userId/friends/:friendId** - Remove a friend

### Thought Routes

- **GET /api/thoughts** - Get all thoughts
- **GET /api/thoughts/:thoughtId** - Get a single thought by ID
- **POST /api/thoughts** - Create a new thought
  ```json
  {
    "thoughtText": "Here's a cool thought!",
    "username": "testuser",
    "userId": "userId"
  }
  ```
- **PUT /api/thoughts/:thoughtId** - Update a thought
- **DELETE /api/thoughts/:thoughtId** - Delete a thought

### Reaction Routes

- **POST /api/thoughts/:thoughtId/reactions** - Add a reaction to a thought
  ```json
  {
    "reactionBody": "I love this thought!",
    "username": "testuser"
  }
  ```
- **DELETE /api/thoughts/:thoughtId/reactions/:reactionId** - Remove a reaction

## Testing with Insomnia

This API is designed to be tested with Insomnia or similar API testing tools. Follow these steps to effectively test the application:

1. **Set up your environment**:
   - Create a new workspace in Insomnia
   - Set up environment variables for base URL and frequently used IDs

2. **Create request collections**:
   - Create separate folders for Users, Thoughts, and Reactions
   - Save each API endpoint as a separate request

3. **Testing workflow**:
   - First create a user with POST /api/users
   - Use the returned user ID in subsequent requests
   - Create thoughts associated with that user
   - Add reactions to thoughts
   - Test friend functionality between users

4. **Validating responses**:
   - Check for appropriate status codes (200, 201, 404, etc.)
   - Verify response data matches expected format
   - Test error handling by sending invalid data


## Technologies Used

- **MongoDB**: NoSQL database for storing user, thought, and reaction data
- **Express.js**: Web framework for building the API
- **Mongoose**: ODM library for MongoDB and Node.js
- **Node.js**: JavaScript runtime environment
- **JavaScript**: Programming language
- **Insomnia**: API testing tool

## License

No project license file is currently provided. Preserve any upstream notices.

## Credits

Developed by treeewzrd

## Questions

For questions or concerns, please contact me:

- GitHub: [treeewzrd](https://github.com/treeewzrd)
- Contact: [GitHub](https://github.com/treeewzrd)
