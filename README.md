# Zen Class Program Database

This project is a MongoDB-based database design for managing a Zen class program. It includes collections for users, CodeKata problem-solving statistics, attendance tracking, topics, tasks, company drives, and mentors.

## Features

- **Users Collection**: Stores user information including their names, emails, and unique IDs.
- **CodeKata Collection**: Tracks the number of problems solved by users.
- **Attendance Collection**: Records attendance status for each user.
- **Topics Collection**: Maintains a list of topics covered in the program.
- **Tasks Collection**: Manages tasks assigned to users and their submission status.
- **Company Drives Collection**: Details of company drives and attendees.
- **Mentors Collection**: Information about mentors and their mentees.

## Database Structure

### Collections

1. **users**
   - `_id`: Unique identifier for each user.
   - `name`: Name of the user.
   - `email`: Email address of the user.

2. **codekata**
   - `_id`: Unique identifier for each record.
   - `user_id`: Reference to the user who solved the problem.

3. **attendance**
   - `_id`: Unique identifier for each record.
   - `user_id`: Reference to the user.
   - `date`: Date of attendance.
   - `status`: Attendance status (e.g., present, absent).

4. **topics**
   - `_id`: Unique identifier for each topic.
   - `title`: Title of the topic.
   - `date`: Date the topic was covered.

5. **tasks**
   - `_id`: Unique identifier for each task.
   - `user_id`: Reference to the user.
   - `submission_date`: Date when the task was submitted.
   - `status`: Submission status (e.g., submitted, not submitted).

6. **company_drives**
   - `_id`: Unique identifier for each company drive.
   - `company_name`: Name of the company.
   - `date`: Date of the drive.
   - `attendees`: Array of user IDs who attended.

7. **mentors**
   - `_id`: Unique identifier for each mentor.
   - `name`: Name of the mentor.
   - `mentees_count`: Number of mentees.

## Queries

The project includes several MongoDB aggregation queries to extract relevant information, such as:

- Finding all topics and tasks for October.
- Counting the number of problems solved by users in CodeKata.
- Retrieving company drives and attendees for placement.


