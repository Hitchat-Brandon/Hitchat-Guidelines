# Hitchat Javascript Coding Style Guidelines


## Initial Setup

Install the following plugins in your IDE (VSCode is preferred, but you can use any IDE, such as Atom, as long as you install the correct packages. For example, prettier-atom is the plugin for the Atom IDE):

- Prettier
- ESLint

The following is a list of useful plugins. Experiment, find the plugins that suit you best, and enhance your workflow:

- Auto Close Tag
- Auto Rename Tag
- Bracket Pair Colorizer
- Debugger for Chrome
- Javascript (ES6) Code Snippets
- TODO Highlight


## Creating a New React App

While create-react-app is good for learning React and setting up smaller projects, it does come with some caveats.

It has dependencies that we don’t need.
If we ever want server-side rendering, it can make things a little difficult.
We can’t change our build configuration - create-react-app handles it for us.

We want complete control over our app, but we don’t want to make our lives any harder. There are a few steps we can take to avoid making things difficult ourselves.


### Setting up a React app with Webpack and Babel

Babel is great for ensuring compatibility across older browsers. We don’t want to have to worry about keeping up with changes to Javascript, but we don’t want to sacrifice any backwards compatibility.

If we don’t have the scripts provided by create-react-scripts, we need our own bundler then. This is where Webpack comes in.

Here are the steps to set up a new React app with Webpack and Babel.

Create your project root folder, and run npm init. Go through the setup process.
Create your project structure, add in your store folders to src if you’re using react-redux

- public
- src
	- assets
		- fonts
		- img
		- vid
	- components
	- pages
- index.js
- index.css
- App.js
- App.css
- App.test.js

Notice how our folder structure is so much simpler and easier to read when we don’t use create-react-app.


#### Add our React packages

npm install --save react react-dom react-router-dom


#### Setup our dev packages for babel and eslint with prettier with the following command (You can also use npm i).

npm install --save-dev @babel/core @babel/plugin-proposal-class-properties @babel/preset-react babel-loader eslint-config-prettier eslint-plugin-prettier eslint-plugin-react eslint-plugin-react-hooks


#### Setup our dev webpack packages with the following command:

npm install --save-dev webpack webpack-cli webpack-dev-server html-webpack-plugin path


#### Setup our loaders

npm install --save styles-loader css-loader file-loader


#### Create our node_modules folder by running npm install.


#### Add in the following files to your project root:

- .babelrc
- .prettierrc
- .eslintrc
- Webpack.config.js


#### Add our scripts to package.json
"webpack-dev-server": "webpack-dev-server",
"dev": "webpack-dev-server --mode=development",
"prod": "webpack --mode=production",


#### Finally, we can start our project with npm run dev


## Resources

These are the Airbnb style guidelines - be sure to go over them

#### General Javascript 
https://github.com/airbnb/javascript


#### React Specific
https://github.com/airbnb/javascript/tree/master/react

































