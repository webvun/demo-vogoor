Demo Vogoor
===========

This demo shows how to install and use Vogoor. [Here](<https://www.vogoor.com>) is the live version.

Create a new folder:<br>
demo-vogoor

Create the following files:<br>
src/index.html<br>
src/styles.css<br>

Put the following code in **src/index.html**:
````js
<html lang="en">
    <head>
        <meta charset="UTF-8">
    </head>
    <link rel="stylesheet" href="styles.css">
    <body >
        <h1 class = "color:red font-size:20px"> A title </h1>
    </body>
</html>
````

In terminal window run the following commands:
````js
    npm init
    npm i vogoor
````

Put the following code, obove the scripts property in package.json file
````js
    "watch": {
        "vogoor": {
        "patterns": [
            "src"
        ],
        "extensions": "html"
        }
    },
````

Put the following code to the scripts property in package.json:
````js
    "watch": "npm-watch",
    "vogoor": "node node_modules/vogoor/build/start.js \"src/styles.css\" \"src\" ",
    "build": "npm run watch vogoor"
````

In terminal window run the following command:
````js
    npm run build
````
