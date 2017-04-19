# Drupal Setup Notes & Instructions
#### By Ash Laidlaw & Benjamin T. Seaver

# Drupal Setup Instructions
1. Navigate to (https://www.drupal.org/project/drupal) and download the Drupal core 7.5.4 (current version as of this readme)
2. Navigate to `project/sites/default` and duplicate the `default.settings.php`, then rename the duplicate to `settings.php`
3. Navigate to the root directory and then change file permissions by typing `chmod -R a+w sites/default`

# Database Setup Instructions
1. Using MAMP, change the server directory to the project's root folder and start the servers
2. Navigate to `http://localhost:8888/phpmyadmin`
3. Create a new database with collation `utf8_general_ci` and click "create"
4. Navigate to the "privileges" section and click "Add user"
   * Enter a username of your choice
   * In the "Host" field, select "local"
   * In the "Password" field, enter your own password (will be used by Drupal site)

# Initial Configuration of Site using Drupal's Web Interface
1. Using MAMP's hosting of the project
2. Navigate to `localhost:8888`
3. Choose `Standard`, `English`
4. Under Database Type choose `MySQL`
5. Fill in database name, the username and password
6. Under `Advanced Options`
   * Host: 127.0.0.1
   * Port: 8889

# Using Git to backup project
* Rename or remove .gitignore
* Save database export into sites/db-backup
   * Export, Custom, Select All tables
   * Save Output to a file, zipped
   * Format SQL, structure and data
   * Object Creation All _except_ `if not exists`


* After cloning repo, import saved database
* If site doesn't load, user may need to be recreated; see `sites/default/settings.php` in your project folder for user name/password
