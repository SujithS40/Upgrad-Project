FILE STRUCTURE
Contact-Bank (root)/
├── client/
│   ├── src
│   ├── public
│   ├── node_modules
│   ├── .env
│   ├── .gitignore
│   ├── package-lock.json
│   └── package.json
├── config
├── models
├── node_modules
├── routes
├── seed
├── .env
├── .gitignore
├── package-lock.json
├── package.json
└── server.js

WORKFLOW
react js -> express.js,node.js -> mongoDB
 mongoDB ->  express.js,node.js -> reactjs

STEPS TO CREATE
1.Clone my github repository.
2. Add your MongoDB connection string from MongoDB as an environment variable.
3.Seed the MongoDB.
4.Enter the package.json scripts.
5. In the root directory CLI npm run dev and everything should run and changes 
   in the UI should be reflected in the database.
6.Serve static assets in production, inside the server.js.

STEPS TO DEPLOYMENT
deploying our app using RENDER 
1. Create a web service in render.
2. Enter the Environment variable for the MongoDB connection string.
3. Create a site.
4. we need Render to use this script to create a build folder from the root npm 
   run render-postbuild and the path to the build folder is ./client/build 
   since all of the npm commands are called in the root folder.
5. In redirects/rewrites our route https://contact-bank.onrender.com/api/* must 
   be the top rule since our routes in the server.js are created with /api/.
6. Then after about 30 minutes the static site link https://contact-bank- 
   a72l.onrender.com/ will be live
