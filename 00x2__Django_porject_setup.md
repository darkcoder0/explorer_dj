# Django Project Environment Setup Guide

## Step 1: Install Python

1. **Download Python**:
   - Go to the [official Python website](https://www.python.org/) and download the latest version suitable for your operating system.

2. **Install Python**:
   - Follow the installation instructions for your operating system.

## Step 2: Install Virtual Environment

1. **Open Command Line Interface**:
   - On Windows, open `Command Prompt` or `PowerShell`.
   - On macOS and Linux, open `Terminal`.

2. **Install `virtualenv`**:
   - Use the following command to install `virtualenv`:
     ```sh
     pip install virtualenv
     ```

## Step 3: Create a Virtual Environment

1. **Navigate to Your Project Directory**:
   - Use `cd` to navigate to the directory where you want to create your Django project.

2. **Create Virtual Environment**:
   - Run the following command to create a virtual environment named `venv`:
     ```sh
     virtualenv venv
     ```

3. **Activate Virtual Environment**:
   - On Windows:
     ```sh
     venv\Scripts\activate
     ```
   - On macOS and Linux:
     ```sh
     source venv/bin/activate
     ```

## Step 4: Install Django

1. **Install Django**:
   - With the virtual environment activated, install Django using pip:
     ```sh
     pip install django
     ```

2. **Verify Django Installation**:
   - Check the Django version to verify the installation:
     ```sh
     django-admin --version
     ```

## Step 5: Start a New Django Project

1. **Create a Django Project**:
   - Use the `django-admin` command to start a new project. Replace `myproject` with your project name:
     ```sh
     django-admin startproject myproject
     ```

2. **Navigate to the Project Directory**:
   - Change directory to your new project:
     ```sh
     cd myproject
     ```

## Step 6: Run the Development Server

1. **Start the Development Server**:
   - Run the following command to start the Django development server:
     ```sh
     python manage.py runserver
     ```

2. **Access the Development Server**:
   - Open a web browser and go to `http://127.0.0.1:8000/` to see your new Django project in action.

## Step 7: Create a Django App

1. **Create an App**:
   - Use the `manage.py` script to create a new app within your project. Replace `myapp` with your app name:
     ```sh
     python manage.py startapp myapp
     ```

2. **Add the App to Settings**:
   - Open `myproject/settings.py` and add your new app to the `INSTALLED_APPS` list:
     ```python
     INSTALLED_APPS = [
         ...
         'myapp',
     ]
     ```

## Step 8: Apply Migrations

1. **Make Migrations**:
   - Create initial migrations for your database schema:
     ```sh
     python manage.py makemigrations
     ```

2. **Apply Migrations**:
   - Apply the migrations to set up your database:
     ```sh
     python manage.py migrate
     ```

## Step 9: Create a Superuser

1. **Create Superuser**:
   - Create an admin user to access the Django admin interface:
     ```sh
     python manage.py createsuperuser
     ```

2. **Follow Prompts**:
   - Enter the required information (username, email, and password) to create the superuser.

## Conclusion

You have successfully set up a Django project environment. You can now start developing your Django application. For more information and tutorials, visit the [official Django documentation](https://docs.djangoproject.com/).

## Additional Tips

- **Deactivate Virtual Environment**:
  - To deactivate the virtual environment, simply run:
    ```sh
    deactivate
    ```

- **Re-activate Virtual Environment**:
  - To re-activate the virtual environment, navigate to your project directory and run the activation command again:
    - On Windows:
      ```sh
      venv\Scripts\activate
      ```
    - On macOS and Linux:
      ```sh
      source venv/bin/activate
      ```

- **After that add requirements.txt file add in root directory**:
   ```sh
      pip freeze > requirements.txt
   ```