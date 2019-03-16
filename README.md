# openBook-website
Website for the openBook project  

The website is currently available as a locally hosted demo.

## Installation Guide

### Tools used
You will need the following tools:
- [Python](https://www.python.org/downloads/)
- [PostgreSQL](https://www.postgresql.org/download/)
- [Virtualenv](https://virtualenv.readthedocs.io/en/latest/installation/)

The hyperlink on each tool's name redirects to its installation instructions for all systems.

### Instructions
**Step 1: Clone repository to your local machine**

Clone the directory:  
`$ git clone https://github.com/openbook-project/openBook-website.git
`  
Go into the repository:  
`$ git clone https://github.com/openbook-project/openBook-website.git
`  

**Step 2: Run the Virtual Environment**

Run the virtual environment with the following commands:  
`$ virtualenv venv`  
`$ source venv/bin/activate`  

The virtual environment should be activated. Your shell should display it like so: `(vnev) $ `.  

**Step 3: Install project dependencies**

Project dependencies are listed in `requirements.txt`. Install them with this command:  
`(venv) $ pip install -r requirements.txt`  

**Step 4: Create a database**  

Enter `postgresql`:
`(venv) $ psql`

The `postgresql` prompt should look like this:  
`psql (version)`  
`Type "help" for help.`  
`username=# `  

Make a new database named `openbook_db` with the following command:
`username=# create database openbook_db`  

A message stating `CREATE DATABASE` should be displayed under the prompt.  

Enter the following to exit `postgresql`:  
`username=# \q`  

**Step 5: Create an environment file**

In this step, we will use a text editor to create a `.env` file. The text editor we will be using is `vim`.  

Create a `.env` file:  
`$ vim .env`  

In the `.env` file, include the following lines:
`DATABASE_URL="postgresql://localhost/openbook_db"
GITHUB_CLIENT_ID="9d9a7da9bfeb288c8a91"
GITHUB_CLIENT_SECRET="08af9bc6a934b25efebf82f68f4a2b40d23b8161"
`

**Step 6: Running flask to locally host the site**

Type the following command to run the `flask` site:  
`(venv) $ flask run`

**Step 7: Viewing the site**

Go to your browser and enter the following address:  
`http://localhost:5000`  

This should display the page in your browser.
