**-Task Manager App Documentation
-Overview**
The Task Manager app is designed to help users efficiently manage their daily tasks by categorizing them and updating their status. The app features user authentication, Firebase Firestore for task storage, and API calls to fetch external content like emojis or GIFs. Users can create new tasks, view and update their status, and categorize them based on deadlines.
Key Features:
**User Authentication:** The app supports user sign-up, sign-in, and password reset using Firebase Authentication. Users must be authenticated to access their tasks.
Task Management: Users can add new tasks, update their status (completed, failed), and organize them by categories such as Today, Upcoming, Completed, and Failed.
Firebase Integration: Task data is stored in Firebase Firestore, ensuring tasks are synced across devices and sessions.
API Calls: The app uses external APIs (such as Giphy) to fetch GIFs and emoji content, adding a fun and interactive element to the user experience.
- How to Use the App
**1. Sign Up / Sign In**
When you open the app for the first time, you will be presented with a sign-in screen.
Sign Up: Enter your email and password and click "Sign Up" to create a new account.
Sign In: If you already have an account, use the "Sign In" option to log in with your email and password.
Password Reset: If you've forgotten your password, click the "Reset Password" button to receive a reset email.

**2. Main Dashboard**
After signing in, you'll be taken to the main dashboard, where you'll see a welcome message and an overview of your tasks for the day.


Task Categories: The app divides tasks into four categories:
Today: Tasks due today.
Upcoming: Tasks with future deadlines.
Task Done: Tasks that have been marked as completed.
Failed: Tasks marked as failed.

**3. Adding a Task**
Click on the Add Task button at the bottom of the screen to create a new task.
Fill out the form: Enter the task title, select a color to categorize the task visually, choose the task type (Basic, Urgent, Important), and set a due date.
Save Task: Click the "Save Task" button to store the task in Firestore.


**4. Viewing and Updating Tasks**
View Tasks by Category: You can switch between task categories using the buttons for Today, Upcoming, Task Done, and Failed.
Update Task Status: For each task, you can either mark it as completed or failed by pressing the appropriate button on the task card.
Task Details: Each task shows its title, due date, and associated color.
5. Task Synchronization
All tasks are automatically saved in Firebase Firestore, ensuring that your tasks are accessible from any device where you are signed in.
Tasks are synced across sessions, so when you return to the app, all your tasks are still available.

**-Authentication and Firebase Integration**
Authentication with Firebase
The app uses Firebase Authentication to handle user sign-up, sign-in, and password management. The authentication process is smooth and secure, ensuring that only registered users can access their tasks.
Sign Up: Firebase Authentication creates a new user account linked to the provided email and password. This information is stored securely in Firebase.
Sign In: Users can log in with their registered email and password. On successful authentication, the app retrieves the user’s tasks from Firestore.
Password Reset: If users forget their password, Firebase sends a password reset email, allowing users to recover their account.

**Firebase Firestore**
The app integrates with Firebase Firestore to store and manage task data. Each task is saved with its title, status, due date, colour, and associated user ID.
Task Creation: When a user creates a new task, the task is stored in Firestore under a unique document ID. This ensures that tasks are stored securely and can be retrieved across devices.
Task Updates: Users can update the status of tasks (e.g., mark them as completed or failed), and these changes are reflected in real-time in the Firestore database.
Task Retrieval: Upon signing in, the app retrieves the user’s tasks from Firestore, ensuring that tasks are synced across sessions.

**API Integration**
The app also utilises APIs to provide additional features:
Giphy API: The app fetches content such as Popcat GIFs or emojis using the Giphy API to add an entertaining and interactive element to the user experience.
Firebase API: Helps use the functions of Firebase authentication and Firebase FireStore features.
	

**-External Source Package:**
The Firebase source package used, which provides different features including Authentication, Analytics and Firestore.
-Handling and Reporting
While error handling is streamlined to ensure a smooth user experience, the app will provide feedback to users if issues arise:
Authentication Errors: If sign-up or sign-in fails (e.g., invalid email or password), the app displays a user-friendly error message.
Task Sync Issues: If there’s an issue with syncing tasks with Firestore (e.g., network problems), the app will inform the user and offer the option to retry.
API Failures: If the Giphy API fails to return content, a fallback message is displayed, ensuring the app continues functioning without major disruptions.

