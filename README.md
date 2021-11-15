# IT TRACKER using redux, materialize and json web server

1. ### `npm create-react-app .` in current folder named "it-tracker"

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
