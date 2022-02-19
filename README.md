# Node - How To

## Instructions
1. Make a new directory (mkdir) and cd into it
2. Type "npm init" in your terminal or "npm init -y" to avoid manual creation
3. Type "touch index.js" in terminal to create our entry point
4. Type "code ." in terminal to open up vscode
5. Type "touch .gitignore" to avoid pushing large files/code to GitHub
6. Type "touch .env" to avoid pushing secret information (i.e., keys)
7. Inside of the .gitignore file, type "node_modules" and ".env"
OR... inside of terminal type "echo node_modules >> .gitignore" and "echo .env >> .gitignore"
8. Type "npm i" to install all of the dependencies if they are already in the code. If not... type "npm i express ejs express-ejs-layouts"
9. IF YOU WANT TO USE EJS, Type "mkdir views" folder and "touch views/layout.ejs views/index.ejs"
10. Type "node index.js" in the terminal of vscode to run the code OR...
11. Type "nodemon" to initiate the nodemon live server
12. Type "nodemon --exec node index.js -e .js, .json, .ejs" so that ejs also runs every time with nodemon OR... you can add '"start": "nodemon--exec node index.js -e .js, .json, .ejs"' to the "scripts" in package.json
13. "control c" to quit nodemon
14. To install a package locally, you want to be at the top level of the folder directory and then type in "npm i 'package'" (for example: npm i dayjs or npm install express)
15. If you look inside of 'package.json' you will now see 'express' or whatever else added on to the dependencies
16. type "killall node" to nodemon running on everything
17. mkdir a folder called "node_modules" if necessary on the top level that will contain information from third party modules
___
## To install a node package globally
- For nodemon... in the command line type: "npm i -g nodemon"
___
## Examples of code inside of index.js
- const myModule = require('./myModule.js')
- const fs = require('fs')
- const express = require('express')
- const ejsLayouts = require('express-ejs-layouts')

___
## Other Examples of Code
- const PORT = 3000/8000/whatever other port you use
- const app = express()
- app.set('view engine', 'ejs')
- app.get('/', (req, res) => {
    res.render('index.ejs')
})

___
## Keep your imports at the top
## Keep your app.listen() at the bottom
___
## app.listen
- app.listen(PORT, (err) => {
    if (err) console.log(err)
    console.log(`listening on port ${PORT}`)
})

## Anatomy of an Express Route
- [express instance].[HTTP verb]([url pattern], [callback])

- app.get(‘/‘, (req, res) => {
	res.send(‘Hello World!’);
});


- And the callback looks like this:
- ([request obj], [response obj]) => {
    // handle data here, if needed
    // call a method from the response object here
}