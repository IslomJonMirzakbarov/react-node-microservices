# React-Node Microservices App 🚀

This repo features a full stack microservices app using React, Node.js, and Express. It demonstrates best practices for scalable and maintainable web development through interconnected services, each handling specific functionality for a modular architecture. The project includes:

- 🖥️ **client**: Frontend part of the application
- 💬 **comments**: Comment management service
- 📨 **event-bus**: Event bus service
- 🛡️ **moderation**: Comment moderation service
- 📝 **posts**: Post management service
- 🔍 **query**: Query service

## Project Structure 🗂️

<pre>
├── 🖥️ client
├── 💬 comments
│   ├── index.js
│   ├── package-lock.json
│   └── package.json
├── 📨 event-bus
│   ├── index.js
│   ├── package-lock.json
│   └── package.json
├── 🛡️ moderation
│   ├── index.js
│   ├── package-lock.json
│   └── package.json
├── 📝 posts
│   ├── index.js
│   ├── package-lock.json
│   └── package.json
├── 🔍 query
│   ├── index.js
│   ├── package-lock.json
│   └── package.json
└── .gitignore
</pre>

## Service Descriptions 📚

### 🖥️ client

This is the frontend part of the application, built with React.

### 💬 comments

This service manages comments for posts. It has the following endpoints:

- `GET /posts/:id/comments`: Fetch all comments for a specific post.
- `POST /posts/:id/comments`: Create a new comment for a specific post.
- `POST /events`: Receive events from other services.

### 📨 event-bus

This service manages event distribution among all services. It has the following endpoint:

- `POST /events`: Distribute an event to all registered services.

### 🛡️ moderation

This service handles comment moderation. It currently has the following endpoint:

- `POST /events`: Receive events from other services.

### 📝 posts

This service manages posts. It has the following endpoints:

- `GET /posts`: Fetch all posts.
- `POST /posts`: Create a new post.
- `POST /events`: Receive events from other services.

### 🔍 query

This service handles querying of post and comment data. It has the following endpoints:

- `GET /posts`: Fetch all posts with their respective comments.
- `POST /events`: Receive events from other services and update the local data.

## .gitignore 🔒

This file lists the files and directories that should not be tracked by Git, including dependencies and miscellaneous files.
