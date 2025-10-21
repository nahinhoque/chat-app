## Real-Time Full Stack Chat Application (Chat-app)
#### A real-time chat application built with MongoDB, Express, React, and Node.js.
#### Messages are delivered instantly using Socket.io. Features signup/signin, real-time user online status, and media messaging. Client and server deployed with Vercel.

### Table of Contents
- #### Purpose & Audience
- #### Project Title & Summary
- #### Installation Prerequisites
- #### Quick Start
- #### Usage Examples
- #### Configuration & Environment
- #### Features & Value
- #### Contributing
- #### License & Authorship
- #### Documentation & Further Reading
- #### Maintenance & Compatibility
- #### Deployment
- #### Changelog & Maintenance Notes
- #### Contact Support


### Purpose & Audience
- #### Provide a practical, real-time chat platform using a modern MERN stack.
- #### Target users: developers wanting to learn, contributors, and end-users who require instant messaging with online status and media messaging capabilities.

### Project Title & Summary
#### Real-Time Full Stack Chat Application (Chat-app)

- #### Tech: MongoDB Atlas, Express, React, Node.js, Socket.io
- #### Real-time bidirectional messaging, online user presence
- #### Authentication with JWT (and/or Clerk integration if used)
- #### Media messaging support
- #### Deployable on GitHub/GitLab with vercel (frontend + backend)

### Installation Prerequisites
  #### - Node.js (LTS) and npm or yarn
  #### - MongoDB Atlas cluster (or local MongoDB)
  #### - Git for version control
  #### - Optional: Cloudinary for media hosting


#### Environment variables 

- ### Backend
  - #### PORT
  - #### MONGO_URI
  - #### CLOUDINARY_CLOUD_NAME
  - #### CLOUDINARY_API_KEY
  - #### CLOUDINARY_API_SECRET
  - #### JWT_SECRET (or equivalent)
  - #### SOCKET_IO_CORS_ORIGIN (if needed)
  - #### CLOUDINARY_CLOUDINARY_FOLDER (optional)

- ### Frontend
  - #### REACT_APP_BACKEND_URL
  - #### VERCEL_ENV 
  - #### Any API keys required by frontend 
 

### Quick Start
#### Client (Frontend) Setup

- #### Create the React project (Vite):
  - #### npm create vite@latest
- #### Rename to Client 
- #### Install dependencies:
  - #### cd Client
  - #### npm install
- #### Start frontend (development):
  - #### npm run dev
- #### Tailwind setup (if using Tailwind):
  - #### npm install tailwindcss postcss autoprefixer
  - #### Follow Tailwind setup steps in your project



### Server (Backend) Setup

- #### Initialize if needed:
  - #### npm init -y
- #### Install dependencies:
  - #### npm install express
  - #### npm install nodemon
  - #### npm install dotenv
  - #### npm install cors
  - #### npm install mongoose
  - #### npm install socket.io
  - #### npm install bcryptjs (for password hashing)
  - #### npm install jsonwebtoken (JWT)
  - #### npm install cloudinary (optional)
  - #### npm install multer (optional for uploads)
- #### Start server (development):
  - #### npm run server
- #### package.json script example:
  - #### "server": "nodemon server.js"
  - #### "start": "node server.js"
 

### Deploy on GitHub / Vercel

- #### Add vercel.json for both client and server if deploying to Vercel
- #### Create separate deployments or a monorepo structure if preferred
- #### Ensure environment variables are set in Vercel dashboard (Backend URL, API keys, etc.)


### Usage Examples
- #### Real-time messaging:
  - #### Client connects to Socket.io server
  - #### Emit and listen for events: "send_message", "receive_message", "user_online", "user_offline"
- #### Online status:
  - #### Emit login/logout events to update presence in real time
- #### Media messages:
  - #### Upload images/videos via Cloudinary and send media URLs in messages
- #### API routes:
  - #### GET /api/users
  - #### POST /api/auth/login
  - #### POST /api/auth/register
  - #### GET /api/messages/:conversationId
  - #### POST /api/messages/:conversationId

#### Frontend routes (example):
  - #### /login, /register
  - #### /chat/:conversationId
  - #### /contacts


### Configuration & Environment
- #### Frontend communicates with Backend via the configured API URL
- #### Socket.io server setup must align with CORS and transport options
- #### Media uploads optionally use Cloudinary
- #### JWT or Clerk for authentication (choose one and configure)
- #### Ensure .env files in backend with required keys and secrets
- #### If using Tailwind, ensure proper setup in the frontend



### Features & Value
  - #### Real-time, bidirectional chat with instant message delivery
  - #### Live presence (online/offline) indicators
  - #### User authentication (signup/signin)
  - #### Media messaging support
  - #### Scalable architecture with MongoDB Atlas and Socket.io
  - #### Clean UI with TailwindCSS
