# New-Project-Setup-Guide
1. create repo on github website and copy ssh link
2. go to terminal and cd into folder we want project
3. type: git clone (ssh repo link)
4. open project in local code editor
5. run terminal to set up package.json:  
npm init -y
6. copy the scrips from this projects package.json to new project
7. run terminal to set up webpack for import/export modules:
npm install webpack webpack-cli --save-dev

8. right click node_modules folder -> git -> add .gitignore file so we don't upload all our modules to github
9. run terminal to get auto refresh browser:
   <br />npm install --save-dev webpack-dev-server

10. create: webpack.config.js -file in global, then copy all code from config file here
11. create a folder named:  "src"
12. inside src folder create files named: index.js
13. create a folder named: "dist"
14. inside dist folder create files named: index.html, style.css
15. link the css and javascript inside the html file with:
  <br>   <script src="myscript.js" defer></script>
   <br>   <link rel="stylesheet" href="style.css">
16. run: npm run watch, or npm run start, for the webpack live server, this builds the main.js file
17. install eslint: 
<br> npm install eslint --save-dev
18. install eslint config file
<br> npm init @eslint/config
19. run to see eslint errors:
<br> npm init @eslint/config
npm run lint
20. run to fix errors:
<br> npm run fix
21. we can set it to auto fix in settings
22. install prettier, we only need to run it for nice format at the end of the project
<br>https://prettier.io/docs/en/install.html
23. now we can start building our project
24. when the projects finished and were ready to deploy on github pages, github looks in the src folder, but our webpack has packed it into the dist folder, so we use this guide so it looks there.
<br> https://gist.github.com/cobyism/4730490
25. install babel to transpile, so es6 javascript works with old browsers
<br> https://babeljs.io/setup#installation
<br> npm install --save-dev @babel/core @babel/preset-env babel-loader
26. after following the guide, babel will work every time webpack saves on watch/server