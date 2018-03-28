# spark-sso-samples
Server-side (Node.JS) and client-side sample apps demonstrating OAuth2 with Cisco Spark REST APIs

## Pre-Requisites

* **NodeJS & NPM** - [Node.js](https://nodejs.org) and [NPM](https://www.npmjs.com/) to install dependencies.  If you do not have Node/NPM installed, see the following guides:
  * Linux: http://blog.teamtreehouse.com/install-node-js-npm-linux
  * Mac: http://blog.teamtreehouse.com/install-node-js-npm-mac
  * Windows: http://blog.teamtreehouse.com/install-node-js-npm-windows  
* **An IDE or developer code editor** - We suggest [Visual Studio Code](https://code.visualstudio.com/), which has great support for debugging Node.JS
* **Git** - Source code management and sharing [Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)

## Running the Samples

1. Create a Cisco Spark 'integration' type application: https://developer.ciscospark.com/apps.html
  * Specify two 'Redirect URI's: http://localhost:8080/oauth and http://localhost:8080/client-side.html
  * Keep the 'Client ID' and 'Client Secret' values visble
2. Use Git to clone the code repo to a directory on your PC, from a terminal window: `git clone https://github.com/CiscoDevNet/spark-sso-samples.git`
3. Change into the repo directory and ask NPM to install needed dependencies:
  ```
  cd spark-sso-samples
  npm install
  ```
4. Open the project in your IDE, for Visual Studio code: `code .`
5. Edit the launch configuration file `.vscode/launch.json`, pasting in the Cisco Spark integration Client ID and Client Secret (be sure and save the file)
6. Run/debug the app (F5) 
  * If not using VS Code, launch via NodeJS, providing the Client ID/Secret via environment variables: 
    ```
    CLIENT_ID={your client id} CLIENT_SECRET={your client secret} node server.js
    ```
7. In a browser, open http://localhost:8080 to access the server-side sample app, and http://localhost:8080/client-side.html to access the client-side app
