# Instructions for setting up React JS Project

# Setting up the client:

## Step 1: Planning

### Application Structure Diagram

### Component Hierarchy Diagram

## Step 2

- Setup React app - npx create-react-app film_releases
- npm start
- Remove app.js return() contents
- Get `<h1> Hello, World!</h1>` displayed on the browser

## Step 3

- Build structure - components / containers
- Set up components, not forgetting imports based on your app hierarchy
- Get something displaying on each component

## Step 4

- Install any libraries you want to use (react router, styled components etc.)

# Setting up the server:

## Structure

```jsx
mkdir server

touch server.js

mkdir db

touch db/seeds.js

mkdir helpers

touch helpers/create_router.js
```

## Installs

```jsx
npm init -y

npm install express

npm install -D nodemon
	then add "server:dev": "nodemon server.js" to the scripts in package.json
	this makes server:dev the command to get the server running in dev mode

npm install cors

npm install mongodb@3.5.7

"mongodb": "^4.7.0
```

## Amend - package.json

```jsx
"scripts": {
"test": "echo \\"Error: no test specified\\" && exit 1",
“start”: “node server.js”,
"server:dev": "nodemon server.js", //ADD
"seeds": "mongosh < db/seeds.js" //ADD
},
```

## Build

- Create seeds in seeds.js
    
- Hook up the database i nserver.js
    
    - Remember app.use(express.json()) to allow the server to accesss the ‘body’
    - Remember app.use(cors()) to avoid cors issues
- npm run seeds → use MongoDB Compass to view the data from your seeds.
    
- Create routes in helpers/create_router.js → use Insomnia to test if each of your routes are working
    

❗ **REMINDER: ADD . GITIGNORE BEFORE PUSHING TO GITHUB**