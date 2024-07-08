# TwitterLikeDatabase

This script creates, manages and analyzes a micro-blogging service database. The database consists of multiple parts, each handling different aspects of the service.

## Part 1: Users Table

1. **Table Creation:** Stores users' details, including first and last name, username, email address, and the date they joined.
2. **Queries:**
    - List usernames and email addresses of all users.
    - List usernames and dates joined for users who joined this year.
    - Count users who joined last year.
    - List user details sorted by last name and first name.
3. **Indexes:**
    - Create an index on the email address.
    - Create an index on last and first names together.
4. **Procedures:**
    - List details of users who joined in a specified year, ordered by date.

## Part 2: Messages Table

1. **Table Creation:** Stores messages posted by users, including the message text, poster's username, and time posted.
2. **Queries:**
    - List the messages and who sent them.
    - List usernames and email addresses of users with their messages.
    - Display a count of messages.
    - Display the percentage of messages sent by a specified user.
    - List users who have sent a message.
3. **Procedures:**
    - List all messages from a specified user, ordered from most to least recent.

## Part 3: Topics and Message Topics Table

1. **Table Creation:**
    - **'topics'** table: Stores topic names and their trending status.
    - **'message_topics'** table: Manages the many-to-many relationship between messages and topics.
2. **Queries:**
    - List trending topics.
    - Create a view listing topic information and messages referring to them.
    - List messages on trending topics, ordered from most recent to least.
3. **Procedures:**
    - List messages and authors for a specified topic.
    - List messages without a topic for a given user.
    - Count messages by a user on a specified topic.

## Part 4: Analytics

1. **Table Creation:** Stores details of users who delete their accounts, including username, date joined, date quit, and the number of messages sent.
2. **Trigger:** Records information when a user is deleted from the **'users'** table.
3. **Procedures:**
    - Get the list of users who quit, their membership duration, and the number of messages sent.

## Sample Data and Tests

- Insertion of sample data for **'users'**, **'messages'**, **'topics'**, and **'message_topics'**.
- Sample queries and procedure calls to test the database functionality.

## Why This Project is Useful

This project provides a comprehensive example of how to design a database for a micro-blogging service similar to Twitter. It includes table creation, indexing, querying, and creating stored procedures to handle various user interactions and data analysis. This makes it an excellent resource for learning and implementing database management skills, SQL querying, and stored procedure creation.

## How to Get Started

Clone the Repository:

```bash
git clone https://github.com/Learner062022/TwitterLikeDatabase.git
cd TwitterLikeDatabase
```
## Set Up the Database

1. Open your preferred MySQL editor (such as MySQL Workbench or paiza.io).
2. Run the SQL scripts provided in the repository to create the database and its tables.

## Insert Sample Data

Use the sample data to populate the database for initial testing.

## Run Queries and Procedures

Execute the sample queries and procedures to understand how to interact with and analyze the data within the database.
