# TaskMatch – Data Model (Simplified ERD in Markdown)

## 📦 Entities & Attributes

### 1. User
- `user_id` (PK)
- `name`
- `email`
- `password_hash`
- `phone_number`
- `user_type` (enum: 'student', 'consumer')
- `school_email_verified` (boolean)
- `created_at`
- `updated_at`

### 2. Task
- `task_id` (PK)
- `title`
- `description`
- `category` (enum: 'lawn', 'delivery', 'tech_help', etc.)
- `location`
- `scheduled_time`
- `budget`
- `status` (enum: 'open', 'assigned', 'completed', 'cancelled')
- `created_by` (FK → User.user_id)
- `assigned_to` (FK → User.user_id, nullable)
- `created_at`
- `updated_at`

### 3. Message
- `message_id` (PK)
- `sender_id` (FK → User.user_id)
- `receiver_id` (FK → User.user_id)
- `task_id` (FK → Task.task_id)
- `content`
- `timestamp`

### 4. Payment
- `payment_id` (PK)
- `payer_id` (FK → User.user_id)
- `payee_id` (FK → User.user_id)
- `task_id` (FK → Task.task_id)
- `amount`
- `status` (enum: 'pending', 'paid', 'failed')
- `timestamp`

### 5. Review
- `review_id` (PK)
- `task_id` (FK → Task.task_id)
- `reviewer_id` (FK → User_
