## How to Restore the `application_db` MongoDB Database Locally

### Prerequisites
- Ensure MongoDB and MongoDB Compass are installed on your local machine.
  - You can download and install MongoDB from the [MongoDB Download Center](https://www.mongodb.com/try/download/community).
  - You can download and install MongoDB Compass from the [MongoDB Compass Download Page](https://www.mongodb.com/products/compass).

### Steps to Restore the Database

1. **Clone the Repository:**
   - Open a terminal or command prompt.
   - Clone this GitHub repository to your local machine by running the following command:
     ```bash
     git clone <repository_url>
     cd <repository_name>
     ```
     Replace `<repository_url>` with the actual URL of the GitHub repository and `<repository_name>` with the name of the repository.

2. **Navigate to the Dump Directory:**
   - Change to the directory where the MongoDB dump files are located:
     ```bash
     cd application_db
     ```

3. **Restore the MongoDB Database using MongoDB Compass:**
   - Open MongoDB Compass.
   - Click on the `Restore` button on the home screen or go to `File` > `Restore`.
   - Select the directory where the dump files are located (`application_db` folder).
   - Choose the `application_db` database to restore.
   - Click on the `Start Restore` button to begin the process.

4. **Verify the Restoration:**
   - In MongoDB Compass, connect to your local MongoDB instance.
   - Navigate to the `application_db` database in the left-hand sidebar to ensure that the collections and their data have been restored correctly.
   - You can explore the collections and documents within `application_db` to verify the data.

### Troubleshooting
- **MongoDB Not Running:** Make sure MongoDB server (`mongod`) is running on your local machine.
- **Permission Issues:** Ensure you have the necessary permissions to read the dump files and to write to MongoDB.
- **Version Compatibility:** Ensure the MongoDB version used to create the dump is compatible with the version you are using to restore it.

### Additional Resources
- [MongoDB Documentation: mongorestore](https://docs.mongodb.com/database-tools/mongorestore/)
- [MongoDB Compass Documentation](https://docs.mongodb.com/compass/current/)
- [MongoDB Installation Guide](https://docs.mongodb.com/manual/installation/)

If you encounter any issues or need further assistance, please contact your nigger.
