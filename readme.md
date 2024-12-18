To set up your PHP programs and HTML files using XAMPP on Ubuntu, follow these steps:

---

### Step 1: **Install XAMPP**
1. **Download XAMPP**:
   - Visit the [XAMPP official website](https://www.apachefriends.org/) and download the latest version of XAMPP for Linux.

2. **Install XAMPP**:
   - Open the terminal and navigate to the directory where the XAMPP installer is downloaded. For example:
     ```bash
     cd ~/Downloads
     ```
   - Make the installer executable:
     ```bash
     chmod +x xampp-linux-x64-*-installer.run
     ```
   - Run the installer:
     ```bash
     sudo ./xampp-linux-x64-*-installer.run
     ```
   - Follow the on-screen installation instructions.

---

### Step 2: **Start XAMPP**
- Start the XAMPP services:
  ```bash
  sudo /opt/lampp/lampp start
  ```
- To stop XAMPP services:
  ```bash
  sudo /opt/lampp/lampp stop
  ```

---

### Step 3: **Set Up Your PHP and HTML Files**
1. **Navigate to the `htdocs` Directory**:
   - XAMPP's web server serves files from the `htdocs` directory:
     ```bash
     cd /opt/lampp/htdocs
     ```

2. **Create Your Project Folder**:
   - Create a new folder for your project:
     ```bash
     sudo mkdir my_project
     ```
   - Set permissions for the folder:
     ```bash
     sudo chmod -R 755 my_project
     ```

3. **Add Your Files**:
   - Copy your PHP and HTML files into the `my_project` folder. For example:
     ```bash
     sudo cp ~/my_files/*.php /opt/lampp/htdocs/my_project/
     sudo cp ~/my_files/*.html /opt/lampp/htdocs/my_project/
     ```

---

### Step 4: **Access Your Project**
1. Open your browser and navigate to:
   ```
   http://localhost/my_project
   ```
2. You should see your PHP and HTML files running.

---

### Step 5: **Check PHP Functionality**
1. Create a test PHP file:
   ```bash
   sudo nano /opt/lampp/htdocs/my_project/test.php
   ```
2. Add the following content:
   ```php
   <?php
   phpinfo();
   ?>
   ```
3. Save and exit (Ctrl + O, Enter, Ctrl + X).
4. Open your browser and go to:
   ```
   http://localhost/my_project/test.php
   ```
   This will display PHP configuration information.

---

### Step 6: **(Optional) Manage XAMPP Through the GUI**
1. Open the XAMPP Control Panel:
   ```bash
   sudo /opt/lampp/manager-linux-x64.run
   ```
2. Use the GUI to start/stop services and manage configurations.

---

You’re all set! Your PHP and HTML files are now ready to be served by XAMPP. Let me know if you encounter any issues.