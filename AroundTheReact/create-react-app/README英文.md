# Create React App [![Build Status][image-1]][1]

Create React apps with no build configuration.
创建一个没有构建配置的React应用。

* [Getting Started][2] – How to create a new app.
* [User Guide][3] – How to develop apps bootstrapped with Create React App.

Create React App works on macOS, Windows, and Linux.<br>
If something doesn’t work, please [file an issue][4].

## Quick Overview

```sh
npm install -g create-react-app

create-react-app my-app
cd my-app/
npm start
```

Then open [http://localhost:3000/][5] to see your app.<br>
When you’re ready to deploy to production, create a minified bundle with `npm run build`.

<img src='https://camo.githubusercontent.com/506a5a0a33aebed2bf0d24d3999af7f582b31808/687474703a2f2f692e696d6775722e636f6d2f616d794e66434e2e706e67' width='600' alt='npm start'>

### Get Started Immediately

You **don’t** need to install or configure tools like Webpack or Babel.<br>
They are preconfigured and hidden so that you can focus on the code.

Just create a project, and you’re good to go.

## Getting Started

### Installation

Install it once globally:

```sh
npm install -g create-react-app
```

**You’ll need to have Node \>= 6 on your machine**. You can use [nvm][6] to easily switch Node versions between different projects.

**This tool doesn’t assume a Node backend**. The Node installation is only required for Create React App itself.

### Creating an App

To create a new app, run:

```sh
create-react-app my-app
cd my-app
```

It will create a directory called `my-app` inside the current folder.<br>
Inside that directory, it will generate the initial project structure and install the transitive dependencies:

```
my-app
├── README.md
├── node_modules
├── package.json
├── .gitignore
├── public
│   └── favicon.ico
│   └── index.html
│   └── manifest.json
└── src
    └── App.css
    └── App.js
    └── App.test.js
    └── index.css
    └── index.js
    └── logo.svg
    └── registerServiceWorker.js
```

No configuration or complicated folder structures, just the files you need to build your app.<br>
Once the installation is done, you can run some commands inside the project folder:

### `npm start` or `yarn start`

Runs the app in development mode.<br>
Open [http://localhost:3000][7] to view it in the browser.

The page will automatically reload if you make changes to the code.<br>
You will see the build errors and lint warnings in the console.

<img src='https://camo.githubusercontent.com/41678b3254cf583d3186c365528553c7ada53c6e/687474703a2f2f692e696d6775722e636f6d2f466e4c566677362e706e67' width='600' alt='Build errors'>

### `npm test` or `yarn test`

Runs the test watcher in an interactive mode.<br>
By default, runs tests related to files changed since the last commit.

[Read more about testing.][8]

### `npm run build` or `yarn build`

Builds the app for production to the `build` folder.<br>
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.<br>
By default, it also [includes a service worker][9] so that your app loads from local cache on future visits.

Your app is ready to be deployed.

## User Guide

The [User Guide][10] includes information on different topics, such as:

- [Updating to New Releases][11]
- [Folder Structure][12]
- [Available Scripts][13]
- [Supported Language Features and Polyfills][14]
- [Syntax Highlighting in the Editor][15]
- [Displaying Lint Output in the Editor][16]
- [Formatting Code Automatically][17]
- [Debugging in the Editor][18]
- [Changing the Page `<title>`][19]
- [Installing a Dependency][20]
- [Importing a Component][21]
- [Code Splitting][22]
- [Adding a Stylesheet][23]
- [Post-Processing CSS][24]
- [Adding a CSS Preprocessor (Sass, Less etc.)][25]
- [Adding Images, Fonts, and Files][26]
- [Using the `public` Folder][27]
- [Using Global Variables][28]
- [Adding Bootstrap][29]
- [Adding Flow][30]
- [Adding Custom Environment Variables][31]
- [Can I Use Decorators?][32]
- [Integrating with an API Backend][33]
- [Proxying API Requests in Development][34]
- [Using HTTPS in Development][35]
- [Generating Dynamic `<meta>` Tags on the Server][36]
- [Pre-Rendering into Static HTML Files][37]
- [Running Tests][38]
- [Developing Components in Isolation][39]
- [Making a Progressive Web App][40]
- [Analyzing the Bundle Size][41]
- [Deployment][42]
- [Advanced Configuration][43]
- [Troubleshooting][44]

A copy of the user guide will be created as `README.md` in your project folder.

## How to Update to New Versions?

Please refer to the [User Guide][45] for this and other information.

## Philosophy

* **One Dependency:** There is just one build dependency. It uses Webpack, Babel, ESLint, and other amazing projects, but provides a cohesive curated experience on top of them.

* **No Configuration Required:** You don't need to configure anything. Reasonably good configuration of both development and production builds is handled for you so you can focus on writing code.

* **No Lock-In:** You can “eject” to a custom setup at any time. Run a single command, and all the configuration and build dependencies will be moved directly into your project, so you can pick up right where you left off.

## Why Use This?

**If you’re getting started** with React, use `create-react-app` to automate the build of your app. There is no configuration file, and `react-scripts` is the only extra build dependency in your `package.json`. Your environment will have everything you need to build a modern React app:

* React, JSX, ES6, and Flow syntax support.
* Language extras beyond ES6 like the object spread operator.
* A dev server that lints for common errors.
* Import CSS and image files directly from JavaScript.
* Autoprefixed CSS, so you don’t need `-webkit` or other prefixes.
* A `build` script to bundle JS, CSS, and images for production, with sourcemaps.
* An offline-first [service worker][46] and a [web app manifest][47], meeting all the [Progressive Web App][48] criteria.

**The feature set is intentionally limited**. It doesn’t support advanced features such as server rendering or CSS modules. The tool is also **non-configurable** because it is hard to provide a cohesive experience and easy updates across a set of tools when the user can tweak anything.

**You don’t have to use this.** Historically it has been easy to [gradually adopt][49] React. However many people create new single-page React apps from scratch every day. We’ve heard [loud][50] and [clear][51] that this process can be error-prone and tedious, especially if this is your first JavaScript build stack. This project is an attempt to figure out a good way to start developing React apps.

### Converting to a Custom Setup

**If you’re a power user** and you aren’t happy with the default configuration, you can “eject” from the tool and use it as a boilerplate generator.

Running `npm run eject` copies all the configuration files and the transitive dependencies (Webpack, Babel, ESLint, etc) right into your project so you have full control over them. Commands like `npm start` and `npm run build` will still work, but they will point to the copied scripts so you can tweak them. At this point, you’re on your own.

**Note: this is a one-way operation. Once you `eject`, you can’t go back!**

You don’t have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn’t feel obligated to use this feature. However we understand that this tool wouldn’t be useful if you couldn’t customize it when you are ready for it.

## Limitations

Some features are currently **not supported**:

* Server rendering.
* Some experimental syntax extensions (e.g. decorators).
* CSS Modules (see [^2285](https://github.com/facebookincubator/create-react-app/pull/2285)).
* Importing LESS or Sass directly ([but you still can use them][52]).
* Hot reloading of components.

Some of them might get added in the future if they are stable, are useful to majority of React apps, don’t conflict with existing tools, and don’t introduce additional configuration.

## What’s Inside?

The tools used by Create React App are subject to change.
Currently it is a thin layer on top of many amazing community projects, such as:

* [webpack][53] with [webpack-dev-server][54], [html-webpack-plugin][55] and [style-loader][56]
* [Babel][57] with ES6 and extensions used by Facebook (JSX, [object spread][58], [class properties][59])
* [Autoprefixer][60]
* [ESLint][61]
* [Jest][62]
* and others.

All of them are transitive dependencies of the provided npm package.

## Contributing

We'd love to have your helping hand on `create-react-app`! See [CONTRIBUTING.md][63] for more information on what we're looking for and how to get started.

## React Native

Looking for something similar, but for React Native?<br>
Check out [Create React Native App][64].

## Acknowledgements

We are grateful to the authors of existing related projects for their ideas and collaboration:

* [@eanplatter][65]
* [@insin][66]
* [@mxstbr][67]

## Alternatives

If you don’t agree with the choices made in this project, you might want to explore alternatives with different tradeoffs.<br>
Some of the more popular and actively maintained ones are:

* [insin/nwb][68]
* [mozilla-neutrino/neutrino-dev][69]
* [jaredpalmer/razzle][70]
* [NYTimes/kyt][71]
* [zeit/next.js][72]
* [gatsbyjs/gatsby][73]
* [electrode-io/electrode][74]

Notable alternatives also include:

* [enclave][75]
* [motion][76]
* [quik][77]
* [sagui][78]
* [roc][79]
* [aik][80]
* [react-app][81]
* [dev-toolkit][82]
* [sku][83]
* [gluestick][84]

You can also use module bundlers like [webpack][85] and [Browserify][86] directly.<br>
React documentation includes [a walkthrough][87] on this topic.

[1]:	https://travis-ci.org/facebookincubator/create-react-app
[2]:	#getting-started
[3]:	https://github.com/facebookincubator/create-react-app/blob/master/packages/react-scripts/template/README.md
[4]:	https://github.com/facebookincubator/create-react-app/issues/new
[5]:	http://localhost:3000/
[6]:	https://github.com/creationix/nvm#installation
[7]:	http://localhost:3000
[8]:	https://github.com/facebookincubator/create-react-app/blob/master/packages/react-scripts/template/README.md#running-tests
[9]:	https://github.com/facebookincubator/create-react-app/blob/master/packages/react-scripts/template/README.md#making-a-progressive-web-app
[10]:	https://github.com/facebookincubator/create-react-app/blob/master/packages/react-scripts/template/README.md
[11]:	https://github.com/facebookincubator/create-react-app/blob/master/packages/react-scripts/template/README.md#updating-to-new-releases
[12]:	https://github.com/facebookincubator/create-react-app/blob/master/packages/react-scripts/template/README.md#folder-structure
[13]:	https://github.com/facebookincubator/create-react-app/blob/master/packages/react-scripts/template/README.md#available-scripts
[14]:	https://github.com/facebookincubator/create-react-app/blob/master/packages/react-scripts/template/README.md#supported-language-features-and-polyfills
[15]:	https://github.com/facebookincubator/create-react-app/blob/master/packages/react-scripts/template/README.md#syntax-highlighting-in-the-editor
[16]:	https://github.com/facebookincubator/create-react-app/blob/master/packages/react-scripts/template/README.md#displaying-lint-output-in-the-editor
[17]:	https://github.com/facebookincubator/create-react-app/blob/master/packages/react-scripts/template/README.md#formatting-code-automatically
[18]:	https://github.com/facebookincubator/create-react-app/blob/master/packages/react-scripts/template/README.md#debugging-in-the-editor
[19]:	https://github.com/facebookincubator/create-react-app/blob/master/packages/react-scripts/template/README.md#changing-the-page-title
[20]:	https://github.com/facebookincubator/create-react-app/blob/master/packages/react-scripts/template/README.md#installing-a-dependency
[21]:	https://github.com/facebookincubator/create-react-app/blob/master/packages/react-scripts/template/README.md#importing-a-component
[22]:	https://github.com/facebookincubator/create-react-app/blob/master/packages/react-scripts/template/README.md#code-splitting
[23]:	https://github.com/facebookincubator/create-react-app/blob/master/packages/react-scripts/template/README.md#adding-a-stylesheet
[24]:	https://github.com/facebookincubator/create-react-app/blob/master/packages/react-scripts/template/README.md#post-processing-css
[25]:	https://github.com/facebookincubator/create-react-app/blob/master/packages/react-scripts/template/README.md#adding-a-css-preprocessor-sass-less-etc
[26]:	https://github.com/facebookincubator/create-react-app/blob/master/packages/react-scripts/template/README.md#adding-images-fonts-and-files
[27]:	https://github.com/facebookincubator/create-react-app/blob/master/packages/react-scripts/template/README.md#using-the-public-folder
[28]:	https://github.com/facebookincubator/create-react-app/blob/master/packages/react-scripts/template/README.md#using-global-variables
[29]:	https://github.com/facebookincubator/create-react-app/blob/master/packages/react-scripts/template/README.md#adding-bootstrap
[30]:	https://github.com/facebookincubator/create-react-app/blob/master/packages/react-scripts/template/README.md#adding-flow
[31]:	https://github.com/facebookincubator/create-react-app/blob/master/packages/react-scripts/template/README.md#adding-custom-environment-variables
[32]:	https://github.com/facebookincubator/create-react-app/blob/master/packages/react-scripts/template/README.md#can-i-use-decorators
[33]:	https://github.com/facebookincubator/create-react-app/blob/master/packages/react-scripts/template/README.md#integrating-with-an-api-backend
[34]:	https://github.com/facebookincubator/create-react-app/blob/master/packages/react-scripts/template/README.md#proxying-api-requests-in-development
[35]:	https://github.com/facebookincubator/create-react-app/blob/master/packages/react-scripts/template/README.md#using-https-in-development
[36]:	https://github.com/facebookincubator/create-react-app/blob/master/packages/react-scripts/template/README.md#generating-dynamic-meta-tags-on-the-server
[37]:	https://github.com/facebookincubator/create-react-app/blob/master/packages/react-scripts/template/README.md#pre-rendering-into-static-html-files
[38]:	https://github.com/facebookincubator/create-react-app/blob/master/packages/react-scripts/template/README.md#running-tests
[39]:	https://github.com/facebookincubator/create-react-app/blob/master/packages/react-scripts/template/README.md#developing-components-in-isolation
[40]:	https://github.com/facebookincubator/create-react-app/blob/master/packages/react-scripts/template/README.md#making-a-progressive-web-app
[41]:	https://github.com/facebookincubator/create-react-app/blob/master/packages/react-scripts/template/README.md#analyzing-the-bundle-size
[42]:	https://github.com/facebookincubator/create-react-app/blob/master/packages/react-scripts/template/README.md#deployment
[43]:	https://github.com/facebookincubator/create-react-app/blob/master/packages/react-scripts/template/README.md#advanced-configuration
[44]:	https://github.com/facebookincubator/create-react-app/blob/master/packages/react-scripts/template/README.md#troubleshooting
[45]:	https://github.com/facebookincubator/create-react-app/blob/master/packages/react-scripts/template/README.md#updating-to-new-releases
[46]:	https://developers.google.com/web/fundamentals/getting-started/primers/service-workers
[47]:	https://developers.google.com/web/fundamentals/engage-and-retain/web-app-manifest/
[48]:	https://github.com/facebookincubator/create-react-app/blob/master/packages/react-scripts/template/README.md#making-a-progressive-web-app
[49]:	https://www.youtube.com/watch?v=BF58ZJ1ZQxY
[50]:	https://medium.com/@ericclemmons/javascript-fatigue-48d4011b6fc4
[51]:	https://twitter.com/thomasfuchs/status/708675139253174273
[52]:	https://github.com/facebookincubator/create-react-app/blob/master/packages/react-scripts/template/README.md#adding-a-css-preprocessor-sass-less-etc
[53]:	https://webpack.js.org/
[54]:	https://github.com/webpack/webpack-dev-server
[55]:	https://github.com/ampedandwired/html-webpack-plugin
[56]:	https://github.com/webpack/style-loader
[57]:	http://babeljs.io/
[58]:	https://github.com/sebmarkbage/ecmascript-rest-spread/commits/master
[59]:	https://github.com/jeffmo/es-class-public-fields
[60]:	https://github.com/postcss/autoprefixer
[61]:	http://eslint.org/
[62]:	http://facebook.github.io/jest
[63]:	CONTRIBUTING.md
[64]:	https://github.com/react-community/create-react-native-app/
[65]:	https://github.com/eanplatter
[66]:	https://github.com/insin
[67]:	https://github.com/mxstbr
[68]:	https://github.com/insin/nwb
[69]:	https://github.com/mozilla-neutrino/neutrino-dev
[70]:	https://github.com/jaredpalmer/razzle
[71]:	https://github.com/NYTimes/kyt
[72]:	https://github.com/zeit/next.js
[73]:	https://github.com/gatsbyjs/gatsby
[74]:	https://github.com/electrode-io/electrode
[75]:	https://github.com/eanplatter/enclave
[76]:	https://github.com/steelbrain/pundle/tree/master/packages/motion
[77]:	https://github.com/satya164/quik
[78]:	https://github.com/saguijs/sagui
[79]:	https://github.com/rocjs/roc
[80]:	https://github.com/d4rkr00t/aik
[81]:	https://github.com/kriasoft/react-app
[82]:	https://github.com/stoikerty/dev-toolkit
[83]:	https://github.com/seek-oss/sku
[84]:	https://github.com/TrueCar/gluestick
[85]:	http://webpack.js.org
[86]:	http://browserify.org/
[87]:	https://reactjs.org/docs/installation.html#development-and-production-versions

[image-1]:	https://travis-ci.org/facebookincubator/create-react-app.svg?branch=master