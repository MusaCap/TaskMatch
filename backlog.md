# 🛠️ TaskMatch – Windsurf Workplan: Epics, Features, User Stories, and Chores

---

## 🌐 EPIC: User Onboarding & Authentication

### Feature: Secure Sign-Up/Login
- **User Story**: As a user, I want to sign up and log in securely using my email and password.
- **Chores**:
  - Implement JWT-based auth service
  - Enable password hashing with bcrypt
  - Create login/signup UI screens
  - School email domain validation for student users

### Feature: User Profile & Verification
- **User Story**: As a student, I want to verify my school affiliation for trust.
- **Chores**:
  - Add student ID & .edu email verification flow
  - Profile picture upload & display
  - Link school email confirmation to user record

---

## 🌐 EPIC: Task Lifecycle Management

### Feature: Post a Task
- **User Story**: As a consumer, I want to post a task with details so I can find local help.
- **Chores**:
  - Create task form UI (title, category, budget, location, schedule)
  - API for task creation & validation
  - Store geolocation data for radius-based matching

### Feature: Browse & Apply to Tasks
- **User Story**: As a student, I want to find nearby tasks I can apply for.
- **Chores**:
  - List open tasks by proximity
  - Filtering by date, category, pay
  - Task apply/interest button + logic

---

## 🌐 EPIC: Communication & Trust

### Feature: In-App Chat
- **User Story**: As a user, I want to chat securely with others before accepting a task.
- **Chores**:
  - Implement socket-based messaging
  - Enable unread message badge counter
  - Build chat history by task ID

### Feature: Ratings & Reviews
- **User Story**: As a user, I want to rate the other party after completing a task.
- **Chores**:
  - Create review form (1–5 stars + optional text)
  - Display reviews in user profile
  - One-time rating submission enforcement

---

## 🌐 EPIC: Payments & Completion

### Feature: Stripe Integration
- **User Story**: As a consumer, I want to pay for completed tasks securely.
- **Chores**:
  - Set up Stripe Connect for student payouts
  - Handle payment hold until task is marked complete
  - Auto-trigger payout upon task closure

### Feature: Task Status Flow
- **User Story**: As a user, I want to track whether my task is open, assigned, or completed.
- **Chores**:
  - Add status column to task table
  - Update UI for each state (e.g. color-coded badges)
  - Create button/action logic for "mark as complete"

---

## 🌐 EPIC: Admin Dashboard & Support

### Feature: Admin Oversight
- **User Story**: As an admin, I want to view and manage all user and task data.
- **Chores**:
  - Admin-only view of all tasks and users
  - Ability to suspend users
  - Reported task moderation queue

---

## 🌐 EPIC: DevOps & QA

### Feature: Testing & Windsurf Tracking
- **Chores**:
  - Integrate GitHub PR automation with Windsurf task status
  - Write unit tests for core APIs
  - Add success metrics logging (task completion, user retention)
