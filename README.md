Set up and go steps

1/ Navigate to your project folder in Terminal (command line etc in Windows).
2/ Run the command "npm init" to initialise an empty repository (You can press enter through all the options it gives you).
3/ Run "npm install node-sass nodemon --save-dev". This will allow you to compile your .scss files to .css.
4/ In your "package.json" file, under "scripts" add the following commands:
  "start": "concurrently \"node app.js\" \"npm run watch-css\" ",
  "build-css": "node-sass --include-path scss src/input.scss src/styles.css",
  "watch-css": "nodemon -e scss -x \"npm run build-css\" "
5/ Back in terminal run "npm install concurrently --save"
6/ Run "npm start" to compile your scss file.
7/ Play.
