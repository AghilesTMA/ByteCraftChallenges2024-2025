# ByteCraft Backend Development Challenge 2024/2025

We are excited to present three levels of backend development challenges. Choose the level that matches your experience and complete the challenge within the deadline.

## 🌱 Beginner Level: User Authentication System

Build a secure user authentication system with essential features.

### Required Features

1. User Registration
2. User Login
3. Protected Routes Access
4. Profile Management

### Technical Requirements

1. Create RESTful API endpoints:
   - Register: `POST /api/auth/register`
   - Login: `POST /api/auth/login`
   - Get Profile: `GET /api/auth/profile`

2. User Data Structure:

```javascript
{
  username: string (required, unique),
  email: string (required, unique),
  password: string (required, min 8 characters),
  fullName: string (required),
  createdAt: timestamp
}
```

3. Implementation Requirements:
   - Password encryption
   - JWT token authentication
   - Input validation
   - Error handling
   - Database integration (MongoDB/PostgreSQL)

### Bonus Features

- Email verification
- Password reset
- Remember me functionality

## 🚀 Intermediate Level: Blog API

Create a fully functional blog API with user interaction features.

### Required Features

1. User Authentication (similar to beginner level)
2. Blog Post Management
3. Comments System
4. Categories
5. Like/Unlike functionality

### Technical Requirements

1. API Endpoints:

```
Posts:
- Create: POST /api/posts
- Read: GET /api/posts
- Update: PUT /api/posts/:id
- Delete: DELETE /api/posts/:id

Comments:
- Add: POST /api/posts/:id/comments
- Get: GET /api/posts/:id/comments
- Delete: DELETE /api/posts/:id/comments/:commentId

Likes:
- Like: POST /api/posts/:id/like
- Unlike: DELETE /api/posts/:id/like
```

2. Data Models Structure:

```javascript
Post {
  title: string (required),
  content: string (required),
  author: ObjectId (reference),
  category: string,
  likes: [ObjectId] (user references),
  createdAt: timestamp
}

Comment {
  content: string (required),
  author: ObjectId (reference),
  post: ObjectId (reference),
  createdAt: timestamp
}
```

3. Implementation Requirements:
   - User authentication
   - Role-based permissions
   - Input validation
   - Error handling
   - Pagination
   - Search functionality

### Bonus Features

- Image upload
- Post drafts
- Tags system
- Post views counter

## 🎯 Advanced Level: Real-time Chat Application

Develop a real-time chat application with rooms and authentication.

### Required Features

1. User Authentication
2. Real-time Messaging
3. Chat Rooms
4. Online Status
5. Message History

### Technical Requirements

1. Implementation:
   - WebSocket integration (Socket.io)
   - Real-time message delivery
   - Room management
   - User presence tracking

2. API Endpoints:

```
Auth:
- Register: POST /api/auth/register
- Login: POST /api/auth/login

Rooms:
- Create: POST /api/rooms
- Join: POST /api/rooms/:id/join
- Leave: POST /api/rooms/:id/leave
- List: GET /api/rooms

Messages:
- Get History: GET /api/rooms/:id/messages
```

3. WebSocket Events:

```javascript
// Client -> Server
'join_room',
'leave_room',
'send_message',
'typing'

// Server -> Client
'receive_message',
'user_joined',
'user_left',
'typing_status'
```

4. Implementation Requirements:
   - Real-time communication
   - Message persistence
   - User presence management
   - Error handling
   - Room access control

### Bonus Features

- Private messaging
- File sharing
- Read receipts
- Message editing/deletion
- User avatars

## General Requirements (All Levels)

1. Code Quality:
   - Clean code structure
   - Proper documentation
   - Error handling
   - Input validation
   - Security best practices

2. Technical Stack:
   - Choose the tech stack you are the most comfortable with.

3. Submission Requirements:
   - GitHub repository
   - README with:
     - Setup instructions
     - API documentation
     - Environment variables list
     - Dependencies list
   - .env.example file
   - Postman/Thunder Client collection (optional)
