# QuickCommerce-test-automation-fe
Quick Commerce proposition automation using Cypress for front end

# Introduction

This project is created to perform the FE regression tests for the Quick Commerce Chain on Acceptance. Below is the structure explained and also how to get this working on your desktop

There are two branches in this project: Master & Dev.

- Master is only used for working code. This is also the branch to run the workflow from
- Dev is used for developing and testing new code. Only merch to the master branch if the new code is stable

# Structure

- config: contains several files that configure the workflows
- fixtures: contains several list with static data that get can be used in a loop (forEach)
- e2e: contains the actual test cases
- plugins: contains the configuration for local runs. When switching from ACC to PROD or vica versa, change the const. file
- support/commands: contains the custom commands for this project
- support/e2e: contains the Import commands for the custom commands. When adding a new file in support/command, this file should also be added to the index.js file

# Installation on desktop

- Install Visual Studio Code (VSC) and install git (https://git-scm.com/downloads)
- Create a folder for this project and clone this repository to it
- Open Visual Studio Code and open the repository
- In the terminal go to the root of the project and install the latest version of npm, Cypress and Cypress-image-snapshot (for visual testing). To do this enter the following commands in the command line:
   npm install -g npm
   npm install cypress --save-dev
   npm install --save-dev cypress-image-snapshot
   Making changes to the code
 - In GitBash go to your project path(for exampel: cd C:\Users\username\Cypress\JumboFindingTeam\finding-test-automation>)
- Change to the Dev branch if you're not already in it
- Fetch and pull by entering the following in the GitBash:
  git fetch
  git pull
- Make the changes and commit your code to the dev branch
- Upload the code to GitHub
- Go to the terminal of Visual Studio Code
- Add all the changes by typing: git add --all
- Commit the changes and write a commit message: git commit -m'upload message'
- Push the changes to the remote branch: git push

# Running test cases on your local/desktop

- Open the terminal in the VSC
- Get to your project path

There are two options: run with the Cypress runner or run headless:

Cypress runner:

- Type the following line in the VSC terminal: npx cypress open --config-file cypress/config/prod-desktop.config.js (change the name of the file to the environment and device you want to test)
- Press enter and wait untill the Cypress runner is opened
- Select Electron 94 as the browser
- Click on the test case you want to run
