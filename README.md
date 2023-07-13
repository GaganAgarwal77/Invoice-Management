# Invoice Management

## Backend
### Creating a virtual environment
To create a virtual environment, run the following commands:

    python3 -m venv venv
    source venv/bin/activate

### Installing dependencies
To install dependencies, run the following command:

    pip install -r requirements.txt

### Setting up MySQL client

Create a new database in MySQL.

### Connecting to MySQL
To connect to MySQL, run the following command:

    mysql -u root -p

### Creating a new database
To create a new database, run the following command:

    CREATE DATABASE <name>;


### Updating the environment variables
To update the environment, run the following commands:

    cd invoicy
    cp .env.example .env

Update the fields in .env file as follows:

    DATABASE_NAME=<db-name>
    DATABASE_USER=<db-user>
    DATABASE_PASS=<db-password>

### Migrating the Database
To migrate the database, run the following commands:

    python3 manage.py makemigrations
    python3 manage.py migrate

### Starting the server
To start the server, run the following command:

    python3 manage.py runserver

## Frontend Setup

    nvm install v12

    nvm use v12

    npm install --legacy-peer-deps

    npm start

## What it does

Our project is an all-in-one platform to manage your invoices. You can create a professional invoice in minutes or pay it in a few clicks. We have created the best user experience with features such as real-time status updates, Multi-level payment model and invoice management.

Our app allows users to:

- Create a company
  - Users can create a company with company name and email
  - We automatically launch metamask and give the option to the user to select their wallet account to sign up with.
  - Through the app, in our navigation we display the status of the wallet (connected/disconnected) and also the wallet address to avoid any confusion.
  
- Add Clients
  - Users are shown a list of companies registered on our app, they can just select the company they want to add as their client.
  
- Discount Clients
  - We provide discount for each client while adding a client. This discount is then directly applied for all the invoices of that client. This helps the company to save time and not try to remember everytime what percentage of discount we gave to that particular client. You can also edit this discount afterwards if needed. This discount is also editables directly in the invoice.
  
- Block Clients
  - A company can block a client , if the client is possibly spamming the company with invoices or for any other reason.
- Create Invoices
  - We autofill the values of the company and the client you select for the invoice for saving the company's time. We also have options for editing advance percent, tax rate and discount rate directly in create invoice.
  
- View Invoices
  - You can see the Invoice as a pdf so that you can store it locally as well. You can download a copy of the invoice directly from the create invoice page as well.

- Pay Invoices
  - We have implemented multi-level payment model where we have 3 options:
    - 100 % Advance : The client has to pay the total value of the invoice before the work is started.
    - X % Advance : The client has to pay X % (As set in create invoice) of total value before the work is started and the rest after work is completed.
    - 100 % Post Work : The client has to pay the total value of the invoice after the work has been completed.
  - We also provide an option to update the work progress in the dashboard itself.
  
- View Status of an Invoice
  - You can view the amount due and work status of the invoice.
- View Statistics of the company
  - We allow companies to see the details of invoices they have generated, pending invoices, amount paid till date, and many other statistics to help the company understand their current situation.

## Built with

- React
- Django