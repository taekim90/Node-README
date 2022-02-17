# Node - How To

## Instructions
1. Make a new directory (mkdir) and cd into it
2. Type "npm init" in your terminal or "npm init -y" to avoid manual creation
3. Type "touch index.js" in terminal to create our entry point
4. Type "code ." in terminal to open up vscode
5. Type "touch .gitignore" to avoid pushing large files/code to GitHub
6. Inside of the .gitignore file, type "node_modules"
7. Type "node index.js" in the terminal of vscode to run the code
8. Type "nodemon" to initiate the nodemon live server
9. "control c" to quit nodemon
10. To install a package locally, you want to be at the top level of the folder directory and then type in "npm i 'package'" (for example: npm i dayjs or npm install express)
11. If you look inside of 'package.json' you will now see 'express' or whatever else added on to the dependencies
___
## Examples of code inside of index.js
- const myModule = require('./myModule.js')
- const fs = require('fs')
