To restore a MongoDB database locally from a dump file, you can use the `mongorestore` command. Here’s how other people can restore the `application_db` database using the dump files you uploaded to GitHub:

### Steps to Restore the Database

1. **Clone the Repository:**
   - First, they need to clone the GitHub repository containing the MongoDB dump files.
   ```bash
   git clone https://github.com/yourusername/your-repo.git
   cd your-repo
   ```

2. **Verify the Dump Directory:**
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

3. **Run `mongorestore`:**
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

### Detailed Steps with Example:

1. **Install MongoDB:**
   - Ensure MongoDB is installed on the local machine. Instructions for installation can be found on the [MongoDB installation guide](https://docs.mongodb.com/manual/installation/).

2. **Clone the Repository:**
   ```bash
   git clone https://github.com/yourusername/your-repo.git
   cd your-repo
   ```

3. **Check the Dump Directory:**
   - Verify that the directory structure is correct:
     ```bash
     ls dump/application_db
     ```
   - You should see BSON and metadata files for the collections.

4. **Restore the Database:**
   ```bash
   mongorestore --db application_db dump/application_db
   ```

5. **Verify the Restoration:**
   - Connect to the MongoDB server and verify that the `application_db` database and its collections are restored.
   ```bash
   mongo
   use application_db
   show collections
   ```

