# ForbiddenTontine

You and your friends have entered into a Tontine, an agreement that the last
living member of your group will gain the wealth of all. What are you willing to
do to ensure that you are the one to take home the prize?

Forbidden Tontine is a game that you play with your friends spanning over the
time of several days or weeks. Each of will try to outlast the others by any means
necessary.

## Local test installation

First you must install Node.js and Mongodb. Go to the Node.js website, download
and install. Mongodb should be able to be installed from a package manager. On a
Mac use brew.

    brew install mongodb

Once these are both installed, in a terminal run

    mongod -dbpath <path/to/ForbiddenTontine/data/db/>

This will start the mongodb server and allow our app to connect to it. In another
terminal go to the ForbiddenTontine base directory. You then need to install the
ForbiddenTontine app through the node package manager (npm).

    npm install

It should install all of the dependencies listed in the package.json file.
You may then start the app with

    npm start

This should start the app running and start the webserver listening on port 3000.
In a browser navigate to http://localhost:3000, or http://127.0.0.1:3000.
You should see the ForbiddenTontine homepage.
