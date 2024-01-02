
# Database and Web Server Setup Script

This script automates the setup of a database server and a web server for an e-commerce application. The script performs the following tasks:

## Database Server Setup

1. **Install and Configure FirewallD:**
   - Install FirewallD.
   - Start and enable the FirewallD service.
   - Check if the FirewallD service is running.

2. **Install and Configure MariaDB:**
   - Install MariaDB server.
   - Start and enable the MariaDB service.
   - Check if the MariaDB service is running.

3. **Configure Firewall Rules for Database:**
   - Add port 3306 to the FirewallD rules.
   - Reload FirewallD to apply the changes.
   - Check if the FirewallD rule for port 3306 is configured.

4. **Configure Database:**
   - Create a database named 'ecomdb'.
   - Create a user 'ecomuser' with the password 'ecompassword'.
   - Grant all privileges to 'ecomuser' on the 'ecomdb' database.
   - Load initial inventory data into the 'products' table.

## Web Server Setup

1. **Install Web Server Packages:**
   - Install Apache HTTP server, PHP, and PHP MySQL extension.

2. **Configure FirewallD Rules for Web Server:**
   - Add port 80 to the FirewallD rules.
   - Reload FirewallD to apply the changes.
   - Check if the FirewallD rule for port 80 is configured.

3. **Update Apache Configuration:**
   - Update the Apache configuration to use index.php as the default page.

4. **Start Apache HTTP Server:**
   - Start and enable the Apache HTTP server.
   - Check if the Apache HTTP service is running.

5. **Download and Configure Web Application:**
   - Install Git.
   - Clone the e-commerce application from the GitHub repository.
   - Update the application code to use 'localhost' instead of a specific IP address.

## Test the Setup

- The script includes a simple test section where it fetches the web page and checks if specific items are present in the page content.

## Usage:

1. Ensure that you have the necessary permissions to execute the script.

2. Run the script:

    ```bash
    ./setup-script.sh
    ```

3. Follow the on-screen instructions and monitor the output for any errors.

**Note:**
- The script uses `sudo`, so ensure that the user running the script has appropriate privileges.

