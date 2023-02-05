#  Creating a React App From Scratch

##  Cited from [here](https://medium.com/@JedaiSaboteur/creating-a-react-app-from-scratch-f3c693b84658)

If you do not install [node.js](https://nodejs.org/en/download/), please download and install  `Node` first.

---
## stage 1

1. project initialize

```
mkdir scratch
cd scratch
npm init
mkdir public src
```
then add a `.gitignore` file excluding (at least) the directories `node_modules `and `dist `

rewrite `package.json` like:

```
{
  "name": "scratch",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "homepage":"./",
  "scripts": {
    "test": "react-scripts test",
    "start": "react-scripts start",
    "build": "react-scripts build"
  },
.....
.
.
.
.....
}
```

After preparation, the `scratch` folder as follows:

```
scratch
├── public
├── src
├── .gitignore
└── package.json
```
2. Create a new `index.html` file in the `public` directory

3. Babel setup
```
npm install --save-dev @babel/core@7.1.0 @babel/cli@7.1.0 @babel/preset-env@7.1.0 @babel/preset-react@7.0.0
```
In the project root, create a file called `.babelrc`. Here, we’re telling babel that we’re going to use the `env` and `react` presets.

4. Webpack setup

```
npm install --save-dev webpack@4.19.1 webpack-cli@3.1.1 webpack-dev-server@3.1.8 style-loader@0.23.0 css-loader@1.0.0 babel-loader@8.0.2
```

Create a new file at the root of the project called `webpack.config.js`. This file exports an object with webpack’s configuration.

5. React

```
npm install --save-dev react@16.5.2 react-dom@16.5.2 react-hot-loader@4.3.11 react-scripts@5.0.0
```

We’ll need to tell our React app where to hook into the DOM (in our `index.html`). Create a file called `index.js` in your `src` directory.

Then, create another file in `src` called `App.js`

Finally, add a really simple stylsheet `App.css` to the `src` directory

---
## stage 2
final project structure should look like the following, unless you changed some names along the way:

```
scratch
├── node_modules
|   ├── ...
|   └── ...
|  
├── public
|   └── index.html 
|  
├── src
|   ├── App.css
|   ├── App.js
|   └── index.js
|
├── .babelrc
├── .gitignore
├── package-lock.json
├── package.json
└── webpack.config.js
```

## Final

```
npm run build
mv build 
```

Upload the folder `build` to the server and rename the folder name to what you want.
