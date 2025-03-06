This project is a Threat Management System that allows users to log in, track cyber threats, manage affected systems, and monitor action statuses based on roles. It is built using Python, Tkinter for the GUI,  and an SQL Server database for data storage.

FEATURES:
User Authentication: Secure login with role-based access control.
Threat Tracking: Add, delete, and manage cyber threats.
Affected Systems Management: Store and retrieve affected system information.
Action Tracking: Monitor actions taken against threats and pending tasks.
GUI Implementation: Tkinter-based user-friendly interface.
Database Integration: Uses SQL Server for storing and managing data.

Technologies Used:
Python
Tkinter (GUI)
PyPyODBC (Database connection)
Microsoft SQL Server

Before running this project, ensure you have:
Python installed (3.x recommended)
Microsoft SQL Server installed and running
Required Python packages installed:
pip install pypyodbc
Database Configuration
Ensure that your SQL Server has a database named db_project and the required tables:
Users (for authentication)
Roles (for user roles and permissions)
Threats (for threat details)
Systems (for affected systems)
AffectedSystems (to map threats to systems)
ThreatActions (for tracking actions taken on threats)
Actions (storing action details)

Update the database connection string in the script as per your server details:
DRIVER_NAME = 'SQL SERVER'
SERVER_NAME = 'YOUR_SERVER_NAME'
DATABASE_NAME = 'db_project'
connection_string = f"""
DRIVER={{{DRIVER_NAME}}};
SERVER={SERVER_NAME};
DATABASE={DATABASE_NAME};
Trust_Connection=yes;
"""

Running the Application
Start SQL Server and ensure the database is accessible.
Run the script in Python:
python your_script.py
The GUI will launch, allowing you to log in and manage threats.

Usage Guide
Login: Enter your username and password to access the system.
Add Affected System: Enter threat and system details to log a new affected system.
Delete Affected System: Remove an affected system by providing its system ID.
View Affected Systems: Display all systems impacted by threats.
Track Actions: View actions taken against various threats.
View Pending Actions: Check pending security measures.

Uses exception handling to manage database errors.
Displays error messages in GUI popups using Tkinter.

Future Enhancements
Implement user role-based access control for enhanced security.
Develop a full-fledged web dashboard using Flask.
Enhance logging mechanisms for better audit trails.

License
This project is open-source and available for modification and distribution.
