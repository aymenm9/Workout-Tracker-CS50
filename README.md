# cs50
cs50 finel project

![OT130Y1](https://github.com/user-attachments/assets/bd5fc357-5d2d-4587-ad17-66c3503f528b)
![7581961](https://github.com/user-attachments/assets/69d20ce0-a71c-40ef-88d7-c3700c60f44b)

# web app WORKOUT TRACKER
#### Video Demo:  <https://youtu.be/s82tZelXQPw>
#### Description:
### Overview
Workout Tracker is a sophisticated web-based fitness application designed to empower users in creating, managing, and tracking personalized workout programs. This application stands out by offering a seamless, interactive user experience through a thoughtful combination of modern web technologies and intuitive design principles.

### Key Technologies
1. **Backend: Flask (Python)**
   - Leveraging the lightweight and flexible Flask framework, the backend provides a robust foundation for handling HTTP requests, managing routes, and orchestrating the application's core logic.
   - Python's simplicity and readability contribute to maintainable and extensible code.

2. **Frontend: HTMX**
   - HTMX, a modern approach to building interactive web applications, allows for dynamic content updates without the complexity of a full JavaScript framework.
   - This choice results in a responsive, single-page-like experience while maintaining the simplicity of server-side rendering.

3. **Database: SQLite3**
   - SQLite3 serves as a lightweight, serverless database solution, perfect for this application's scope.
   - Utilizing CS50's SQL module simplifies database interactions without the overhead of a full ORM, striking a balance between functionality and simplicity.

### Core Features

1. **User Management**
   - Secure user registration and authentication system.
   - Personalized user profiles to track individual progress and preferences.

2. **Fitness Programs**
   - ability to create multiple fitness programs, catering to different goals or time periods.
   - Each program can be customized with a name, description, and target completion date.

3. **Workouts**
   - Programs are divided into individual workouts, allowing for structured planning.
   - Users can schedule workouts, assign them to specific days, and track completion.

4. **Exercises**
   - Detailed exercise definitions within each workout.
   - Users can specify exercise names, target repetitions, sets, and optionally, weights or duration.

5. **Progress Tracking**
   - Comprehensive tracking system allowing users to monitor their progress at program, workout, and exercise levels.
   - Visual indicators and statistics to motivate users and provide insights into their fitness journey.

### Technical Deep Dive

#### File Structure and Functionality
1. `app.py`: The main Flask application file, serving as the entry point and configuration hub.
2. `__init__.py`: Package initialization file, ensuring proper module imports.
3. `db.py`: Handles database connection and provides an interface for database operations.
4. `auth.py`: Contains crucial authentication-related functions:
   - `signup_user`: Manages new user registration.
   - `login_user`: Handles user authentication.
   - `login_required`: A decorator to restrict access to authenticated users.
   - `htmx_required`: Ensures certain routes are only accessible via HTMX requests.
5. `db.sql`: SQL script for initial database schema creation.
6. `workout.db`: The SQLite3 database file storing all application data.
7. `routes/home.py`: Manages the main UI routes, including home, program, and workout views.
8. `routes/program.py`: Contains routes and logic for program management.
9. `routes/__init__.py`: Initializes the routes package.

#### Design Choices and Rationale
1. **HTMX for Frontend Interactivity**
   - Chosen for its simplicity and seamless integration with Flask.
   - Provides a modern, dynamic user experience without the learning curve of complex JavaScript frameworks.

2. **CS50 SQL Module**
   - Opted for direct SQL interactions instead of an ORM like SQLAlchemy.
   - Reduces unnecessary complexity for a smaller-scale application while maintaining full control over database operations.

3. **Custom Authentication**
   - Implemented bespoke login and signup functionality instead of using Flask-Login or Flask-Form.
   - This approach allowed for a more tailored user experience and helped in understanding the underlying mechanics of web authentication.

4. **Bootstrap for Styling**
   - Utilized to rapidly develop a visually appealing and consistent user interface.
   - Ensures responsiveness across various devices and screen sizes.

### User Guide
1. Clone the project repository to your local machine.
2. Install the required dependencies using `pip install -r requirements.txt`.
3. Initialize the database by running the SQL script in `db.sql`.
4. Start the application with `flask run`.
5. Navigate to the provided local URL to access the Workout Tracker.
6. Register a new account or log in if returning.
7. Create your first fitness program, add workouts, and define exercises.
8. Use the tracker to log your progress as you complete workouts and exercises.

### Future Enhancements
1. **URL Flexibility**: Implement a routing system that allows users to start from any URL, not just the root.
2. **UI Improvements**: Enhance the styling of program and workout pages for a more polished look.
3. **Error Handling**: Integrate more comprehensive error messaging, particularly on the login page.
4. **Mobile App**: Develop a companion mobile application for on-the-go tracking.
5. **Social Features**: Implement sharing capabilities and community challenges to increase engagement.
6. **Data Visualization**: Add charts and graphs to visually represent progress over time.
7. **Exercise Library**: Create a pre-populated exercise database to assist users in workout creation.

### Conclusion
Workout Tracker stands as a testament to the power of combining simple, effective technologies to create a practical, user-friendly application. By focusing on core functionality and user experience, this app provides fitness enthusiasts with a valuable tool to organize, track, and improve their workout routines. Whether you're a beginner starting your fitness journey or an experienced athlete looking to optimize your training, Workout Tracker offers the flexibility and features to support your goals.
