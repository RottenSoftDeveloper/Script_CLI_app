Script 1: CLI APP

**Scripts Made Simple**

**Overview**

This Python script provides a simple, interactive menu-driven tool for managing and executing scripts from designated folders. It includes features for logging, script execution, and menu-based navigation, designed for streamlined usage and error handling.

**Features**

Interactive Menu: Navigate through folders and scripts using a user-friendly menu interface.
* Script Execution: Run individual scripts, multiple scripts, or all scripts within selected folders.
* Logging: Logs all script executions and errors to separate log files for tracking and debugging.
* Reloading: Refresh the list of scripts dynamically.
* Log Viewing: View recent execution logs directly within the application.

**Prerequisites**

* Python 3.12 or later: The script is configured to use Python 3.12's pythonw.exe.
* tqdm: For progress bars.
* Scripts Directory: Ensure your scripts are located in designated folders specified in the script.

**Installation**

1. Clone or download this repository.
2. Install the required dependencies using:

          pip install tqdm

3. Place your Python scripts in the designated folders defined in the folders dictionary.

**Configuration**

The script uses the following configuration:

1. Folders: Modify the folders dictionary in the main() function to include paths to your script directories:

    folders = {
    "Accounts": r"c:\Users\Administrator\Documents\Py scripts\WORKER\Accounts",
    "ActiveDir": r"c:\Users\Administrator\Documents\Py scripts\WORKER\ActiveDir",
      }

2. Log Paths: Update the paths for log files if needed:

 script_log_path = r"C:\Users\Administrator\Documents\Py scripts\MASTER\logs\script_log.txt"
info_log_path = r"C:\Users\Administrator\Documents\Py scripts\MASTER\logs\info_log.txt"
size_log_path = r"C:\Users\Administrator\Documents\Py scripts\MASTER\logs\size_log.txt"

3. Python Executable: The script uses pythonw.exe to run scripts without a console. Update the path if your Python installation is different:

        ["C:\\Path\\To\\Python\\pythonw.exe", script_path]

**Usage**
1. Run the script:
    python script_manager.py

2. Select options from the menu to:
* Navigate to folders.
* Execute scripts.
* View logs.
* Reload scripts.
* Exit the application.

**Menu Options**
* List of Folders: Navigate to scripts in the respective folders.
* Run All Scripts: Execute all scripts across all folders.
* Reload Scripts: Refresh the script list dynamically.
* View Recent Logs: Display logs directly in the console.
* Exit: Quit the program.

**Logging**

The script maintains logs in three files:
* script_log.txt: Tracks script executions.
* info_log.txt: Provides detailed logs, including errors.
* size_log.txt: Reserved for special script logs (e.g., PGsize-specific).

**Error Handling**
* Errors during script execution are logged with timestamps and formatted for readability.
* Logs are flushed immediately to ensure up-to-date information.

**Disclaimer**
Use this tool responsibly. Ensure that the scripts you execute are safe and free from malicious code. Always review and test scripts before running them in production environments.


“Please Run Responsibly :]”

Script 2: PostgreSQL to CSV Exporter

```markdown
# PostgreSQL to CSV Exporter

A Python script to export data from a PostgreSQL table into a CSV file. The script connects to a PostgreSQL database, executes a query to retrieve data, and writes the results into a specified CSV file.

---

## 🚀 Features

- **Data Export**: Exports data from a PostgreSQL table to a CSV file.
- **Custom Queries**: Easily modify the SQL query to export specific data.
- **Automatic CSV Headers**: Includes table column names as CSV headers.

---

## 🛠 Prerequisites

- **Python 3.x** installed on your system.
- Required Python libraries:
  - `psycopg2`
- Access to a PostgreSQL database.

---

## 📥 Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/postgres-to-csv-exporter.git
   cd postgres-to-csv-exporter
   ```

2. Install dependencies:
   ```bash
   pip install psycopg2
   ```

3. Update the script with your PostgreSQL connection details and query.

---

## ⚙️ Configuration

### Database Connection

Edit the following details in the script:

```python
# PostgreSQL connection details
conn = psycopg2.connect(
    dbname="Cylerian",
    user="dave",
    password="!1950!DpD!",
    host="127.0.0.1",
    port="5432"
)
```

### SQL Query

Modify the SQL query to select data from your desired table:

```python
# Execute SQL query to select data
cur.execute("SELECT * FROM Highgate-Vulnerabilities")
```

### CSV File Path

Set the path for the output CSV file:

```python
# Write rows to CSV file
with open('C:\\Users\\Administrator\\Documents\\Py scripts\\highgate_vulnerabilities.csv', 'w', newline='') as f:
    ...
```

---

## ▶️ Usage

1. Run the script:
   ```bash
   python postgres_to_csv.py
   ```
2. The script will:
   - Connect to the PostgreSQL database.
   - Execute the specified SQL query.
   - Write the query results into a CSV file.

---

## 📁 Directory Structure Example

```plaintext
postgres-to-csv-exporter/
│
├── postgres_to_csv.py
├── requirements.txt
├── README.md
└── output/
    └── highgate_vulnerabilities.csv
```

---

## 📊 Output

- **CSV Export**:
  - The specified PostgreSQL table is exported to a CSV file.
- **File Location**:
  - The CSV file is saved to the specified path, e.g.:
    ```plaintext
    C:\Users\Administrator\Documents\Py scripts\highgate_vulnerabilities.csv
    ```

---

## 🔔 Notes

- Ensure the table name and SQL query are valid for your PostgreSQL database.
- Verify file paths and permissions to avoid issues during CSV creation.

---

## 📜 License

This project is licensed under the [MIT License](LICENSE).

---

## 🧑‍💻 Author

 _“Automate smarter, not harder.”_
```
