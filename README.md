1. **Download the Repository:**
   - Your teammate should clone the GitHub repository where you have uploaded the MongoDB dump files (`application_db`).

2. **Install MongoDB:**
   - Ensure MongoDB is installed and running on their local machine. They can download MongoDB from the [official MongoDB website](https://www.mongodb.com/try/download/community).

3. **Restore the MongoDB Dump:**
   - Open a terminal or command prompt.
   - Navigate to the directory where the MongoDB dump files (`application_db`) are located (the directory where they cloned the GitHub repository).
   - Use the `mongorestore` command to import the database dump into their local MongoDB instance:
     ```
     mongorestore --db application_db /path/to/dump/directory/application_db
     ```
     - Replace `/path/to/dump/directory` with the actual path where the `application_db` dump directory is located within the cloned repository.

4. **Verify Database Import:**
   - Once `mongorestore` completes, verify that the `application_db` database has been imported successfully into their local MongoDB instance.

5. **Start MongoDB Service:**
   - Ensure the MongoDB service is running on their local machine. They can start MongoDB using appropriate commands for their operating system (`mongod` or `sudo service mongod start` on Unix-based systems).

6. **Connect to the Database:**
   - Modify your application's database connection settings to point to the local MongoDB instance (`localhost:27017` by default).

