# Build an AI web app by using Python and Flask
Use Python, Flask, and Azure Cognitive Services to build a web app that incorporates AI

# Set up a development environment
To get started writing our Flask application with Python, we need to set up our development environment, which will require a couple of items to be installed. Fortunately, the tools we'll use are relatively common, so they'll serve you well even beyond this module. You might even have them installed! We'll use these tools to develop and test your application locally.

In this unit, you'll learn how to install Python tooling and create a virtual Python environment. You'll install Flask, which is the framework we'll use for creating the website.

At a high level, we'll perform the following steps:
1. Install Visual Studio Code (if not already installed)
2. Install Python (if not already installed)
3. Create a directory for your code
4. Create a virtual environment
5. Install Flask and other libraries

# Create the project directory
Create a directory in the location of your choice. This directory will be your project directory, and will contain all of the code we'll create. You can create a directory from a command or terminal window with one of the following commands:

 ## Windows
    md contoso
    cd contoso

 ## macOS or Linux
    mkdir contoso
    cd contoso

# Create a Python virtual environment
A Python virtual environment isn't necessarily as complex as it sounds. Rather than creating a virtual machine or container, a virtual environment is a folder that contains all of the libraries we need to run our application, including the Python runtime itself. By using a virtual environment, we make our applications modular, allowing us to keep them separate from one another and avoid versioning issues. As a best practice you should always use virtual environments when working with Python.

To use a virtual environment, we'll create and activate it. We create it by using the venv module, which you installed as part of your Python installation instructions earlier. When we activate it, we tell our system to use the folder we created for all of its Python needs.

  ## Windows
    // Create the environment
    python -m venv venv
    // Activate the environment
    .\\venv\\scripts\\activate

 ## macOS or Linux
    // Create the environment
    python3 -m venv venv
    // Activate the environment
    source ./venv/bin/activate

# Install Flask and other libraries
1.In the command or terminal window, run the following command to open the directory in Visual Studio Code:
    code .
2.select New File, Name the file requirements.txt, and add the following text:
    flask
    python-dotenv
    requests
3.Return to the command or terminal window and perform the installation by using pip to run the following command:
    pip install -r requirements.txt

# Create an app
We're going to create our application iteratively, focusing on specific concepts as we go. To start, we'll create the landing page for our application, which will display the form the user will use.

Typically, the entry point for Flask applications is a file named app.py. We're going to follow this convention and create the core of our application. We'll perform the following steps:

1. Create our core application
2. Add the route for our application
3. Create the HTML template for our site
4. Test the application

# Create core application
1. create a new file named app.py by clicking New file in the Explorer tab
2. Add the code to create your Flask application
    from flask import Flask, redirect, url_for, request, render_template, session
    app = Flask(__name__)
The import statement includes references to Flask, which is the core of any Flask application. We'll use render_template in a while, when we want to return our HTML.

app will be our core application. We'll use it when we register our routes in the next step.



