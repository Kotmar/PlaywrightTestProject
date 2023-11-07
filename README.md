Repository for [BUG] Output folder is not cleaned before execution tests using "Run Tests"/"Run Test" in VS Code Playwright extension

Explicitly commited test-results folder.
To reproduce this bug it is enough to create default project with `npm init playwright@latest` command, then create file in `test-results` folder and execute example tests. 
If tests are executed using `Run Tests` then created file in `test-results` folder will NOT be removed before test run.
If tests are executed using `Debug Tests` then created file in `test-results` folder will be removed before test run.

Context:

Playwright Version: 1.35.0, 1.39.0
Operating System: Windows
Node.js version: v18.15.0
Visual Studio Code version: 1.84.0
Playwright for VSCode extension version: 1.0.17
Browser: Chrome
Extra: -
Steps to reproduce:

Write initial data in output test folder. In current case default folder was used: './test-results'
Execute tests via "Run Tests"/"Run Test" button in VS Code Playwright extension
Observe that data in output test folder is not cleaned
Actual result:
Data in output test folder is not cleaned before run.

Expected result:
Data in output test folder must be cleaned before run.

Note: "Debug Tests"/"Debug Test" works fine (data in output test folder is cleaned before run)
