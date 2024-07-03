To restore a MongoDB database locally from a dump file, you can use the `mongorestore` command. Here’s how other people can restore the `application_db` database using the dump files you uploaded to GitHub:

### Steps to Restore the Database

1. **Install MongoDB:**
   - Ensure MongoDB is installed on the local machine. Can download from [MongoDB Community Server Download](https://www.mongodb.com/try/download/community#:~:text=MongoDB%20Community%20Server%20Download). Make sure to check the install MongoDB Compass option during setup, it should be checked by default. Can watch this video from start until 5.45min to see how to install: https://www.youtube.com/watch?v=OiMOQr457Qs
   - Need to download MongoDB tools to be able to use mongorestore. If you do not have the MongoDB tools installed, you can click on [this](https://fastdl.mongodb.org/tools/db/mongodb-database-tools-windows-x86_64-100.9.5.zip) to download. After downloading the ZIP file, extract it.
Add the extracted directory to your system's PATH environment variable to access the tools from any command prompt by:

1. Open the Start menu, search for "Environment Variables," and select "Edit the system environment variables."
2. In the System Properties window, click on the "Environment Variables" button.
3. Under the "System variables" section, scroll down and select the "Path" variable, then click "Edit."
4. In the Edit Environment Variable dialog, click "New" and add the path to the extracted MongoDB tools directory (e.g., C:\path\to\mongodb-database-tools-windows-x86_64-100.9.5\bin).
5. Click "OK" to close all dialog boxes.

2. **Clone the Repository:**
   - First, they need to clone the GitHub repository containing the MongoDB dump files.
   ```bash
   git clone https://github.com/yourusername/your-repo.git
   cd your-repo
   ```

3. **Verify the Dump Directory:**     
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

4. **Run `mongorestore`:**
   - Use the `mongorestore` command to restore the database from the dump directory. They should specify the path to the directory containing the dump files.
   ```bash
   mongorestore --db application_db /path/to/dump/application_db
   ```
   - Replace `/path/to/dump/application_db` with the actual path to the dump directory. If the current directory is the repository root, the command would be:
   ```bash
   mongorestore --db application_db dump/application_db
   ```

5. **Verify the Restoration:**

Open MongoDB Compass:

Launch MongoDB Compass on your local machine.



Connect to Your Local MongoDB Instance:

In MongoDB Compass, click on the "Connect" button to connect to your local MongoDB instance. The default connection string is usually mongodb://localhost:27017.



Check the database:

Go to the application_db database and check that the collections are created with the data inside.

