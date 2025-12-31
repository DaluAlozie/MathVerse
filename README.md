# MathVerse 🎮📚

**MathVerse** is a full-stack, real-time educational web platform designed to make learning mathematics interactive, engaging, and social.  
It combines arcade-style gameplay, multiplayer functionality, class management tools, and a moderated discussion system into a single cohesive application.

The platform is built using a modern client–server architecture with real-time communication, persistent data storage, and role-based access control.

---

## ✨ Core Features

### 🎮 Interactive Learning Game
- 2D arcade-style game that integrates maths questions into gameplay
- Single-player and real-time multiplayer modes
- Competitive leaderboards and timed challenges
- Server-authoritative game logic to prevent cheating
- Support for user-created custom games

### 🧑‍🏫 Class & Group Management
- Create and manage learning groups
- Invite and approve users
- Assign and remove games from groups
- Track participation and engagement

### 💬 Discussion & Q&A System
- Thread-based forum for maths questions and explanations
- Image uploads, tagging, and search
- Sorting and filtering by activity and relevance
- Reporting system for inappropriate content

### 🔔 Notification System
- Real-time notifications for:
  - Forum replies
  - Group invitations
- Inbox with read/unread tracking
- Filtering and search functionality

### 🛡️ Moderation & Role System
- Role-based permissions (Admin, Moderator, User)
- Content filtering for inappropriate language
- Reporting, moderation, deletion, and restoration tools
- Designed with safety, accountability, and data integrity in mind

---

## 🧱 Tech Stack

### Frontend
- **HTML** – semantic markup
- **CSS** – responsive layout and UI styling
- **JavaScript** – client-side logic and UI interactions
- **Canvas API** – real-time game rendering

### Backend
- **Python**
- **Flask** – backend framework
- **Flask-SocketIO** – real-time WebSocket communication

### Database
- **SQLite**
- Relational schema for users, games, groups, forum posts, and roles
- Custom ORM-style abstraction layer

### Architecture
- Client–server architecture
- RESTful API endpoints for data operations
- WebSockets for real-time multiplayer and notifications
- JSON-based communication between client and server

---

## 🕹️ Real-Time Multiplayer Architecture

- Multiplayer games are **server-authoritative**
- Game state is synchronised using **WebSockets**
- Only necessary state deltas are transmitted to minimise bandwidth
- Supports multiple concurrent game sessions
- Ensures fairness and consistency across clients

---

## 🗂️ Project Structure

```txt
MathVerse/
├── static/            # CSS, JavaScript, images
├── templates/         # HTML templates
├── app.py             # Flask application entry point
├── database.py        # Database and data access logic
├── playGame.py        # Game engine and mechanics
├── utilities.py       # Shared helper functions
├── badwordsAPI.py     # Content filtering logic
├── createDatabase.py  # Database initialisation
├── Users.db           # SQLite database
└── README.md
