# IT TRACKER using redux, materialize and json web server

1. ### `npx create-react-app .` in current folder named "it-tracker"

2. ### `npm i -D json-server concurrently`

In the root of application add a file named "db.json" This will hold our data.
This dummy data will act as a server and will update accordingly. "logs" and "techs".

3. ### Add the following scripts to package.json which will allow to listen to json server and run concurrently.

"json-server": "json-server --watch db.json --port 5000",
"dev": "concurrently \"npm start\" \"npm run json-server\"",

4. ### `npm run dev`
5. ### Add proxy in package.json at bottom so we don't have to deal with localhost 5000 in the requests in the react front end, the restart the server.

   "proxy": "http://localhost:5000"

6. ### `npm install materialize-css@next`
7. ### `npm run dev` then clean up react app as usual.
   turn app.js into a function, get rid of css in app.css
8. ### import 'materialize-css/dist/css/materialize.min.css';
   ### import M from 'materialize-css/dist/js/materialize.min.js';
   bring in the main css and js files to application in App.js
9. ### ` useEffect(() => { M.AutoInit();});`
   Bring into App.js ---- This allows us to use modals and other components of Materialize since we can not access query selectors in React.
10. ### `<link href="https://fonts.googleapis.com/css2?family=Material+Icons"rel="stylesheet">`
    search for material ui icons grab link. Add to index.html, change title to it logger.
11. ### Start building components and layout, fetch data from json web server.
12. ### `npm i moment react-moment`
    import it in the LogItem.js file
13. ### Continue to add folders/files building application
14. # REDUX
### `npm i redux react-redux redux-thunk redux-devtools-extension`

### redux - a state management library 
### react-redux - a package that allows redux to work with react.
### redux-thunk - a piece of middleware for redux which allows for asynchronous functions inside of actions so we can wait for response to comeback and dispatch to the reducer.
### redux-devtools-extension - allows for cleaner code to be written to enable the dev tools in chrome for redux.    

# Bring Redux into a component.

# Add new functionality to the app.

1. Add the action.

2. Add reducer functionality.

3. Connect to the component.