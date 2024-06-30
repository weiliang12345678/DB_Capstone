To restore a MongoDB database locally from a dump file, you can use the `mongorestore` command. Here’s how other people can restore the `application_db` database using the dump files you uploaded to GitHub:

### Steps to Restore the Database

1. **Install MongoDB:**
   - Ensure MongoDB is installed on the local machine. Instructions for installation can be found on the [MongoDB installation guide](https://docs.mongodb.com/manual/installation/). Can watch this video from start until 5.45min to see how to install: https://www.youtube.com/watch?v=OiMOQr457Qs
   
2. **Clone the Repository:**
   - First, they need to clone the GitHub repository containing the MongoDB dump files.
   ```bash
   git clone https://github.com/yourusername/your-repo.git
   cd your-repo
   ```

3. **Verify the Dump Directory:**
      - Verify that the directory structure is correct:
     ```bash
     ls dump/application_db
     ```
   - You should see BSON and metadata files for the collections.
     
   - Ensure the directory contains the dump files for the `application_db` database. The structure should look something like this:
     ```
     your-repo/
     └── dump/
         └── application_db/
             ├── collection1.bson
             ├── collection1.metadata.json
             ├── collection2.bson
             └── collection2.metadata.json
     ```

5. **Run `mongorestore`:**
   - Use the `mongorestore` command to restore the database from the dump directory. They should specify the path to the directory containing the dump files.
   ```bash
   mongorestore --db application_db /path/to/dump/application_db
   ```
   - Replace `/path/to/dump/application_db` with the actual path to the dump directory. If the current directory is the repository root, the command would be:
   ```bash
   mongorestore --db application_db dump/application_db
   ```
If you do not have the MongoDB tools installed, you can download them separately from the MongoDB website. Here’s how you can install the MongoDB tools, including mongorestore:
For Windows:
Go to the [MongoDB Download Center](https://www.mongodb.com/try/download/database-tools#:~:text=MongoDB%20Command%20Line%20Database%20Tools%20Download).
Select your version and platform.
Download the ZIP file and extract it.
Add the extracted directory to your system's PATH environment variable to access the tools from any command prompt.

6. **Verify the Restoration:**

Open MongoDB Compass:

Launch MongoDB Compass on your local machine.



Connect to Your Local MongoDB Instance:

In MongoDB Compass, click on the "Connect" button to connect to your local MongoDB instance. The default connection string is usually mongodb://localhost:27017.



Check the database:

Go to the application_db database and check that the collections are created with the data inside.

