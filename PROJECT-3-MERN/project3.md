# My task is to implement a web solution based on MERN stack in AWS cloud

## MERN web stack consists of the following components

- MongoDB: A document-based, No-SQL database used to store application data in a form of documents.
- ExpressJS: A server side Web Application framework for Node.js.

- ReactJS: A frontend framework developed by Facebook. It is based on JavaScript, used to build User Interface (UI) components.

- Node.js: A JavaScript runtime environment. It is used to run JavaScript on a machine rather than in a browser.

# STEP 1 - BACKEND CONFIGURATION

- Update ubuntu by runnig:

`sudo apt update`

![ubuntu-update](./ubuntu-update.PNG)

- I upgraded ubuntu by running this command:

`sudo apt upgrade`

- This command upgrades to the latest version and discard the old version while update command update and still keep the old version

![ubuntu-upgrade](./ubuntu-upgrade.PNG)

- I Installed Node.js with the command below

`sudo apt-get install -y nodejs`

-Note: The command above installs both nodejs and npm. NPM is a package manager for Node like apt for Ubuntu, it is used to install Node modules & packages and to manage dependency conflicts.

![nodejs-install](./nodejs-install.PNG)

- I verified node is installed by running the command below

`node -v`

![node-verify](./node-verify.PNG)

- I verified npm is installed by running this command

`npm -v`

![npm-verify](./npm-verify.PNG)

- I created a new directory for my To-Do project:

`mkdir Todo`

- I changed my current directory to the newly created directory:

`cd Todo`

- Next, I used the command npm init to initialise my project, so that a new file named package.json will be created. This file will normally contain information about my application and the dependencies that it needs to run. Follow the prompts after running the command. I pressed Enter several times to accept default values, then accept to write out the package.json file by typing yes.

`npm init`

![init](./initial.PNG)
