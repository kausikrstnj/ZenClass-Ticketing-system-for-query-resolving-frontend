﻿# ZenClass-Ticketing-system-for-query-resolving-frontend

## Auth Routes

### Sign In
- **Route**: `/auth/signin`
- **Method**: `POST`
- **Description**: Authenticates a user.
- **Controller**: `authController.signin`

### Sign Out
- **Route**: `/auth/signout`
- **Method**: `GET`
- **Description**: Signs out a user.
- **Controller**: `authController.signout`

## Query Routes

### Create Query
- **Route**: `/api/createQuery`
- **Method**: `POST`
- **Description**: Creates a new query.
- **Middleware**: None
- **Controller**: `queryController.create`

### List Queries
- **Route**: `/api/queries/:userId/:role`
- **Method**: `GET`
- **Description**: Retrieves all queries based on user ID and role.
- **Middleware**: None
- **Controller**: `queryController.list`

### View Query
- **Route**: `/api/query/:queryId`
- **Method**: `GET`
- **Description**: Retrieves details of a specific query.
- **Middleware**: None
- **Controller**: `queryController.view`

### Get Mentors
- **Route**: `/api/mentors`
- **Method**: `GET`
- **Description**: Retrieves a list of all available mentors.
- **Middleware**: None
- **Controller**: `queryController.getMentors`

### Assign Mentor
- **Route**: `/api/assignMentor/:mentorId/:queryId`
- **Method**: `PUT`
- **Description**: Assigns a mentor to a specific query.
- **Middleware**: None
- **Controller**: `queryController.assignMentor`

### Close Query
- **Route**: `/api/closeQuery/:queryId`
- **Method**: `PUT`
- **Description**: Closes a query by the mentor.
- **Middleware**: None
- **Controller**: `queryController.closeQuery`

### Get All Assigned Queries
- **Route**: `/api/getAllAssignedQueries`
- **Method**: `GET`
- **Description**: Retrieves all assigned queries.
- **Middleware**: None
- **Controller**: `queryController.getAllAssignedQueries`

## User Routes

### Get All Users and Create User
- **Route**: `/api/users`
- **Method**: 
  - `GET`: Retrieves all users.
  - `POST`: Creates a new user.
- **Middleware**: `authenticateToken` for retrieving all users.
- **Controllers**:
  - `GET`: `userController.list`
  - `POST`: `userController.create`

### User Profile Operations
- **Route**: `/api/users/:userId`
- **Method**: 
  - `GET`: Retrieves user profile by ID.
  - `PUT`: Updates user profile by ID.
  - `DELETE`: Deletes user profile by ID.
- **Middleware**: None
- **Controllers**:
  - `GET`: `userController.read`
  - `PUT`: `userController.update`
  - `DELETE`: `userController.remove`

### View User Profile Data
- **Route**: `/api/users/profile/:userId`
- **Method**: `GET`
- **Description**: Retrieves specific user profile data.
- **Middleware**: None
- **Controller**: `userController.profileData`

### Save Reset Token
- **Route**: `/api/resetToken`
- **Method**: `PUT`
- **Description**: Saves a reset token in the database.
- **Middleware**: None
- **Controller**: `userController.randomNumber`

### Verify Email
- **Route**: `/api/verifyEmail/:userId`
- **Method**: `POST`
- **Description**: Verifies user email.
- **Middleware**: None
- **Controller**: `userController.verifyEmail`

### Change Password
- **Route**: `/api/changePassword/:userId`
- **Method**: `PUT`
- **Description**: Changes user password.
- **Middleware**: None
- **Controller**: `userController.changePassword`


