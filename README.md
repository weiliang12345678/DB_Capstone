## How to Restore the `application_db` MongoDB Database Locally

### Prerequisites
- Ensure MongoDB and MongoDB Compass are installed on your local machine. You can download and install them from the [MongoDB Download Center](https://www.mongodb.com/try/download/community).
- YouTube video of how to download, watch until 5.00 min (https://www.youtube.com/watch?v=gB6WLkSrtJk)

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

3. **Restore the MongoDB Database Using MongoDB Compass:**
   - Ensure MongoDB is running on your local machine. 
   - Open MongoDB Compass.
   - Click on the "Connect" button to connect to your local MongoDB instance. The default connection string is:
     ```
     mongodb://localhost:27017
     ```
   - Once connected, click on the "Databases" tab.
   - Click the "Create Database" button.
   - Enter `application_db` as the database name and provide a collection name (e.g., `temp_collection` can be deleted later). This will create an empty database.
   - Now, import the BSON files:
     - Click on the newly created database `application_db`.
     - Click on the "Collections" tab.
     - Click the "Add Data" button and select "Import File".
     - For each collection (e.g., `analyses.bson` and `users.bson`):
       - Choose "BSON" as the import format.
       - Select the corresponding `.bson` file.
       - Click on "Import" to import the data into the respective collection.

4. **Verify the Restoration:**
   - In MongoDB Compass, navigate to the `application_db` database and check that the collections (e.g., `analyses`, `users`) are present and the data is correctly imported.

### Troubleshooting
- **MongoDB Not Running:** Make sure MongoDB server (`mongod`) is running on your local machine.
- **Import Errors:** Ensure you selected the correct import format (BSON) and file for each collection.

### Additional Resources
- [MongoDB Compass Documentation](https://docs.mongodb.com/compass/current/)
- [MongoDB Installation Guide](https://docs.mongodb.com/manual/installation/)

If you encounter any issues or need further assistance, please contact limpeh.
