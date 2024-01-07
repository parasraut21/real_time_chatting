# Real-Time Chat Application
## Introduction
Welcome to the Real-Time Chat Application, a project by Paras Raut – a passionate full-stack developer and blockchain enthusiast. This application enables secure and real-time communication between users, offering an engaging chat experience.

## Features
User Authentication: Secure login and registration processes to protect user data.
Avatar Personalization: Users can choose avatars to personalize their profiles.
Real-Time Chat: Engage in dynamic conversations with real-time updates.
Typing Indicators: View when contacts are typing, enhancing user interaction.
Online/Offline Status: Easily identify the online/offline status of contacts.

## Components
**1. Home (Landing Page)**
Displays the title and purpose of the application.
**2. Login Component**
Provides a secure login for accessing chat features.
**3. Register Component**
Guides users through a secure registration process.
Utilizes toasts for information verification.
Allows avatar selection for personalized profiles.
**4. Avatar Selection**
Users can choose avatars to personalize their profiles.
**5. Chatting Component**
**Contacts Section:**
Displays a list of contacts with online/offline status.
Indicates when contacts are typing.
**Chat Interface**:
Real-time conversation updates.
Typing indicators for contacts.

## Backend Storage
MongoDB database securely stores user information, messages, and online/offline statuses.
Efficient data management for seamless communication

## Technology Stack
Frontend
React
Styled Components
Socket.IO for real-time communication
Backend
Express
MongoDB for data storage
Socket.IO for real-time event handling

# Getting Started

**Live App Demo** : [https://www.idurarapp.com/demo-erp-crm/](https://www.idurarapp.com/demo-erp-crm/)

```
🚀 Give a Star ⭐️ & Fork to this project ... Happy coding! 🤩`
```

## Getting started

#### Step 1: Clone the repository

```bash
https://github.com/parasraut21/real_time_chatting.git
```

```bash
cd real_time_chatting
```

#### Step 2: Create Your MongoDB Account and Database/Cluster

- Create your own MongoDB account by visiting the MongoDB website and signing up for a new account.

- Create a new database or cluster by following the instructions provided in the MongoDB documentation. Remember to note down the "Connect to your application URI" for the database, as you will need it later. Also, make sure to change `<password>` with your own password

- add your current IP address to the MongoDB database's IP whitelist to allow connections (this is needed whenever your ip changes)

#### Step 3: Edit the Environment File

- Check a file named .env in the /backend directory.

  This file will store environment variables for the project to run.

#### Step 4: Update MongoDB URI

In the .env file, find the line that reads:

`DATABASE="your-mongodb-uri"`

Replace "your-mongodb-uri" with the actual URI of your MongoDB database.

#### Step 5: Install Backend Dependencies

In your terminal, navigate to the /backend directory

```bash
cd server
```

the urn the following command to install the backend dependencies:

```bash
npm install
```

This command will install all the required packages specified in the package.json file.

#### Step 6: Run Setup Script

While still in the /backend directory of the project, execute the following command to run the setup script:

```bash
npm run setup
```

This setup script may perform necessary database migrations or any other initialization tasks required for the project.

#### Step 7: Run the Backend Server

In the same terminal, run the following command to start the backend server:

```bash
npm run start
```

This command will start the backend server, and it will listen for incoming requests.

#### Step 8: Install Frontend Dependencies

Open a new terminal window , and run the following command to install the frontend dependencies:

```bash
cd ui
```

```bash
npm install
```

#### Step 9: Run the Frontend Server

After installing the frontend dependencies, run the following command in the same terminal to start the frontend server:

```bash
npm run start
```

This command will start the frontend server, and you'll be able to access the website on localhost:3000 in your web browser.

:exclamation: :warning:` If you encounter an OpenSSL error while running the frontend server, follow these additional steps:`

Reason behind error: This is caused by the node.js V17 compatible issues with OpenSSL, see [this](https://github.com/nodejs/node/issues/40547) and [this](https://github.com/webpack/webpack/issues/14532) issue on GitHub.

Try one of these and error will be solved

- > upgrade to Node.js v20.

- > Enable legacy OpenSSL provider

Here is how you can enable legacy OpenSSL provider

- On Unix-like (Linux, macOS, Git bash, etc.)

```bash
export NODE_OPTIONS=--openssl-legacy-provider
```

- On Windows command prompt:

```bash
set NODE_OPTIONS=--openssl-legacy-provider
```

- On PowerShell:

```bash
$env:NODE_OPTIONS = "--openssl-legacy-provider"
```

Here is [reference](https://github.com/webpack/webpack/issues/14532#issuecomment-947012063) about enabling legacy OpenSSL provider

After trying above solutions, run below command

```bash
npm run start
```

> If you still facing issue, then follow [this stackoverflow thread](https://stackoverflow.com/questions/69692842/error-message-error0308010cdigital-envelope-routinesunsupported). It has so many different types of opinions. You definitely have solution after going through the thread.
