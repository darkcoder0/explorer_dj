## How to Setup Python and Set Environment variables

# Python Installation Guide

## Step 1: Download Python

1. **Open a Web Browser**:
   - Open your preferred web browser (e.g., Chrome, Firefox, Safari).

2. **Navigate to the Official Python Website**:
   - Go to the official Python website: [python.org](https://www.python.org/).

3. **Access the Downloads Page**:
   - On the homepage, click on the `Downloads` tab.

4. **Select Your Operating System**:
   - The website automatically suggests the best version for your operating system. Click on the `Download Python` button to download the latest version.

## Step 2: Install Python

### Windows

1. **Run the Installer**:
   - Locate the downloaded file (usually in the `Downloads` folder) and double-click to run the installer.

2. **Add Python to PATH**:
   - In the installer window, check the box that says `Add Python 3.x to PATH`.

3. **Start Installation**:
   - Click on `Install Now` to start the installation process.

4. **Complete Installation**:
   - Once the installation is complete, you will see a `Setup was successful` message. Click on `Close` to finish.

### macOS

1. **Run the Installer**:
   - Locate the downloaded `.pkg` file (usually in the `Downloads` folder) and double-click to run the installer.

2. **Follow the Instructions**:
   - Follow the on-screen instructions. Click `Continue` and `Agree` to accept the license agreement.

3. **Install Python**:
   - Click `Install` to begin the installation. You may need to enter your administrator password.

4. **Complete Installation**:
   - Once the installation is complete, you will see a `The installation was successful` message. Close the installer.

### Linux

1. **Open Terminal**:
   - Open your terminal application.

2. **Update Package List**:
   - Update your package list by running:
     ```sh
     sudo apt update
     ```

3. **Install Python**:
   - Install Python by running:
     ```sh
     sudo apt install python3
     ```

4. **Verify Installation**:
   - Verify the installation by checking the Python version:
     ```sh
     python3 --version
     ```

## Step 3: Verify Python Installation

1. **Open Command Line Interface**:
   - On Windows, open `Command Prompt` or `PowerShell`.
   - On macOS, open `Terminal`.
   - On Linux, open your terminal application.

2. **Check Python Version**:
   - Type the following command and press `Enter`:
     ```sh
     python --version
     ```
   - You should see the installed Python version displayed.

## Step 4: Install pip (Python Package Installer)

1. **Ensure pip is Installed**:
   - pip is included with Python installation from version 3.4 onwards. Verify pip installation by running:
     ```sh
     pip --version
     ```
   - If pip is not installed, you can install it by running:
     ```sh
     python -m ensurepip --upgrade
     ```

## Step 5: Install a Python Package

1. **Use pip to Install a Package**:
   - You can install Python packages using pip. For example, to install the `requests` package, run:
     ```sh
     pip install requests
     ```

## Conclusion

You have successfully downloaded and installed Python on your system. You can now start writing and running Python scripts. For more information and tutorials, visit the [official Python documentation](https://docs.python.org/3/).



