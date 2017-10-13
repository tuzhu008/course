这个项目是由 [Create React App][1] 引导的.

下面你将找到一些关于如何执行常见任务的信息。 <br>
你可以找到这个指南的最新版本 [here][2].

## 包含内容

- [ 更新到最新版本 ][3] 
- [ 发送反馈 ][4] 
- [ 文件夹结构 ][5] 
- [ 可用脚本 ][6] 
  - [npm start][7]
  - [npm test][8]
  - [npm run build][9]
  - [npm run eject][10]
- [支持的语言特性和兼容的旧设备][11]
- [编辑器高亮][12]
- [在编辑器显示 Lint 输出][13]
- [编辑器调试][14]
- [自动格式化代码][15]
- [改变页面`<title>`][16]
- [安装依赖][17]
- [导入组件][18]
- [代码分割][19]
- [添加样式表][20]
- [后处理 CSS][21]
- [添加CSS预处理器 (Sass, Less etc.)][22]
- [添加 Images, Fonts, 和 Files][23]
- [使用`public` 文件夹][24]
  - [改变 HTML][25]
  - [添加模块系统外的资源][26]
  - [何时使用 `public` 文件夹][27]
- [使用全局变量][28]
- [添加 Bootstrap][29]
  - [使用自定义主题][30]
- [添加 Flow][31]
- [添加自定义环境变量][32]
  - [在HTML中引用环境变量][33]
  - [在Shell中添加临时环境变量][34]
  - [在 `.env`中添加开发环境变量][35]
- [使用修饰符吗?][36]
- [ 与API后端集成 ][37]
  - [Node][38]
  - [Ruby on Rails][39]
- [在开发中代理 API 请求][40]
  - [出现”Invalid Host Header" 错误后配置代理][41]
  - [手动配置代理][42]
  - [配置一个Websocket代理][43]
- [在开发中使用 HTTPS][44]
- [在服务器中生成动态 `<meta>` 标签][45]
- [预渲染到静态HTML 文件][46]
- [ 从服务器向页面中注入数据 ][47]
- [运行测试][48]
  - [文件名的约定][49]
  - [命令行接口][50]
  - [版本控制一体化][51]
  - [编写测试][52]
  - [测试组件][53]
  - [使用三方断言库][54]
  - [初始化测试环境][55]
  - [聚焦和排除测试][56]
  - [覆盖率报告][57]
  - [持续集成][58]
  - [禁用 jsdom][59]
  - [快照测试][60]
  - [编辑器集成][61]
- [隔离开发组件][62]
  - [开始使用故事书][63]
  - [开始使用Styleguidist][64]
- [制作一个渐进的 Web App][65]
  - [选择缓存][66]
  - [首先考虑][67]
  - [渐进的 Web App Metadata][68]
- [分析包的大小][69]
- [部署][70]
  - [静态服务器][71]
  - [其他解决方案][72]
  - [ 使用客户端路由服务应用程序 ][73]
  - [Building的相对路径][74]
  - [Azure][75]
  - [Firebase][76]
  - [GitHub Pages][77]
  - [Heroku][78]
  - [Netlify][79]
  - [Now][80]
  - [S3 and 云字体][81]
  - [Surge][82]
- [高级配置][83]
- [故障排除][84]
  - [`npm start` 没有发生变化][85]
  - [`npm test` hangs on macOS Sierra][86]
  - [`npm run build` 过早退出][87]
  - [`npm run build` 在 Heroku上发生错误][88]
  - [`npm run build` 在 minify发生错误][89]
  - [Moment.js locales 消失][90]
- [Something Missing?][91]

## Updating to New Releases
更新到新版本。
Create React App 分为两个包:

* `create-react-app` 是一个全局命令行工具，用于创建新项目.
* `react-scripts` 是生成的项目中的一个开发依赖关系(已包含).

你几乎不需要更新 `create-react-app` 本身: 它把所有的设置都委托给了 `react-scripts`.

当你运行 `create-react-app`, 它总是使用最新版的 `react-scripts`来创建项目， 这样你就可以自动获得新创建的应用程序的所有新功能和改进。

将现有的项目更新为一个新版本的 `react-scripts`, [打开更新日志][92], 找到你目前正在做的版本(如果你不确定，打开文件夹检查 `package.json`文件), 并为新版本应用迁移说明.

大多数情况下， `react-scripts` 版本 在 `package.json` 中，在此目录下运行 `npm install` 就够了,但是还是需要参考一下 [changelog][93] 来获得潜在的破坏性的改变。

我们承诺保持最低限度的改变 ，这样你就可以毫无痛苦地升级`react-scripts` 

## Sending Feedback
发送反馈。
我们总是开放 [your feedback][94].

## Folder Structure
文件夹结构
创建完成后, 你的项目大概是这样的:

```
my-app/
  README.md
  node_modules/
  package.json
  public/
    index.html
    favicon.ico
  src/
    App.css
    App.js
    App.test.js
    index.css
    index.js
    logo.svg
```

对于要构建的项目 ** 这些文件必须以确切的文件名存在**:

* `public/index.html`  是页面模板;
* `src/index.js` 是 JavaScript 入口点.

您可以删除或重命名其他文件.

你可以在 `src`里面创建子目录. 为更快的重建, 只有在 `src` 里的文件是由Webpack处理的.<br>
你需要 ** 把JS和CSS文件放在`src`里面 **, 否则 Webpack 不会看到它们.

只有 `public` 里的文件才能被 `public/index.html`使用.<br>
下面是使用JavaScript和HTML的资源的阅读说明.

但是，您可以创建更多的顶级目录 <br>
它们不会被包含在生产构建中所以你可以用它们来做文档.

## Available Scripts
可用的脚本
在项目目录中，您可以运行:

### `npm start`

在开发模式下运行应用.<br>
打开 [http://localhost:3000][95] 在浏览器中查看

如果你进行编辑，页面会重新加载.<br>
您还将在控制台中看到任何lint错误.

### `npm test`

在交互式观察模式下启动测试运行程序.<br>
请参阅 [运行测试][96] 部分以获得更多信息.

### `npm run build`

构建生产模式的应用到 `build` 文件夹.<br>
它在生产模式中正确地捆绑了响应，并优化了构建以获得最佳性能.

构建是缩小的，文件名包括散列。 <br>
你的应用已经准备好部署了！

参阅 [deployment部署][97] 以获取更多信息。

### `npm run eject`

**注意: 这是一个单向操作.一旦 `eject`,就无法返回!**

如果您对构建工具和配置选项不满意，您可以随时`eject`。该命令将从您的项目中删除单个构建依赖项。

相反，它会将所有的配置文件和传递依赖项(Webpack、Babel、ESLint等)复制到你的项目中，这样你就可以完全控制它们了。除`eject`之外的所有命令仍然有效，但是它们将指向复制的脚本，以便您可以对它们进行调整。在这一点上，你k可以按自己的来.

你不需要使用 `eject`. 精心设计的特性集适合于小型和中型部署，您不应该感到有义务使用该特性。但是我们知道，如果您不能在准备好时定制它，那么这个工具就不会有用了。

## Supported Language Features and Polyfills
支持的语言特性和兼容
这个项目支持最新的JavaScript标准的超集。 <br>
除了 [ES6][98] 语法特性,它还支持:

* [Exponentiation Operator][99] 求幂运算符 (ES2016).
* [Async/await][100] 异步(ES2017).
* [Object Rest/Spread Properties][101] (stage 3 proposal).
* [Dynamic import()][102] 动态导入(stage 3 proposal)
* [类和静态属性][103]  class 和 const (part of stage 3 proposal).
* [JSX][104] and [Flow][105] 语法.

了解更多[不同方案阶段 ][106].

尽管我们建议使用的是实验性的，但Facebook在产品代码中大量使用这些功能， 所以我们打算提供 [codemods代码插件][107] 如果这些建议中的任何一项在未来改变.

注意 ** 这个项目只包括一些ES6 [兼容][108]**:

* [`Object.assign()`][109] via [`object-assign`][110].
* [`Promise`][111] via [`promise`][112].
* [`fetch()`][113] via [`whatwg-fetch`][114].

如果您使用其他需要的ES6+特性 **实时运行支持** (例如 `Array.from()` or `Symbol`), 确保您已经手动地包含了适当的兼容，或者您所针对的浏览器已经支持它们了。

## Syntax Highlighting in the Editor
编辑器语法高亮
要在您最喜欢的文本编辑器中配置突出显示的语法, 前往 [相关的Babel文档页面][115] 并遵循指示. 一些受欢迎的编辑器被涵盖。

## Displaying Lint Output in the Editor
编辑器显示Lint输出
> 注意: 在 `react-scripts@0.2.0` 和更高版本上，这个特性是可用的 <br>
> 它只能在 npm 3 或更高版本上工作.

一些编辑器, 包括 Sublime Text, Atom, 和 Visual Studio Code, 都提供ESlint插件。.

它们不是用来做衬线的。您应该在终端和浏览器控制台中看到linter输出。但是，如果您希望在编辑器中出现lint结果，那么您可以执行一些额外的步骤.

您需要为您的编辑器首先安装一个ESLint插件. 然后添加一个文件叫做 `.eslintrc` 的文件到项目根目录:

```js
{
  "extends": "react-app"
}
```

现在您的编辑器应该报告linting警告.

注意， 即使你进一步编辑的你的 `.eslintrc` 文件，这些改变 **编辑器的集成**. 它们不会影响终端和浏览器内的lint输出。这是因为，创建响应应用程序有意提供了一套最小的规则集，可以找到常见的错误。

如果您想为您的项目强制执行编码风格，请参考使用 [Prettier][116] 而不是ESLint样式规则
## Debugging in the Editor
编辑器调试
**这个特性目前只支持[Visual Studio Code][117] 和 [WebStorm][118].**

Visual Studio Code 和 WebStorm 支持Create React App 进行调试. 这使您可以作为开发人员在不离开编辑器的情况下编写和调试您的React代码，最重要的是，它使您能够拥有一个持续的开发工作流程，在这种情况下，上下文切换是最小的，因为您不必在工具之间切换。

### Visual Studio Code

你需要安装最新版本的 [VS Code][119] and VS Code [Chrome调试器扩展][120].

然后把下面的代码块加入到 `launch.json` 文件中 ，然后将其放入到应用根目录的`.vscode` 文件夹.

```json
{
  "version": "0.2.0",
  "configurations": [{
    "name": "Chrome",
    "type": "chrome",
    "request": "launch",
    "url": "http://localhost:3000",
    "webRoot": "${workspaceRoot}/src",
    "userDataDir": "${workspaceRoot}/.vscode/chrome",
    "sourceMapPathOverrides": {
      "webpack:///src/*": "${webRoot}/*"
    }
  }]
}
```
> 注意: 如果通过[HOST 或 PORT 环境变量][121] 进行调整，URL可能会有所不同 

Start your app by running `npm start`, and start debugging in VS Code by pressing `F5` or by clicking the green debug icon. You can now write code, set breakpoints, make changes to the code, and debug your newly modified code—all from your editor. 运行`npm start`启动你的应用程序，并通过按`F5`或单击绿色调试图标开始在VS代码中进行调试。现在，您可以编写代码、设置断点、对代码进行更改，并从编辑器中调试新修改的代码。

### WebStorm

你需要安装 [WebStorm][122] 和 [JetBrains IDE Support][123] 的Chrome扩展。
在WebStorm的 `Run` 菜单中选择`Edit Configurations...`. 然后单击 `+` 并选择 `JavaScript Debug`. 将 `http://localhost:3000` 粘贴在URL字段中，并保存配置. 

> 注意: 如果通过[HOST 或 PORT 环境变量][124] 进行调整，URL可能会有所不同 .

运行 `npm start`开启应用, 然后在 macOS 上按 `^D` 或者在Windows and Linux上按 `F9` 或绿色调试按钮来在WebStorm中开始调试。

The same way you can debug your application in IntelliJ IDEA Ultimate, PhpStorm, PyCharm Pro, and RubyMine. 
同样的方法，你可以在IntelliJ IDEA Ultimate, PhpStorm, PyCharm Pro, and RubyMine中调试你的应用
## Formatting Code Automatically
自动格式化
Prettier 是一个固定风格的代码格式器，支持 JavaScript, CSS and JSON. 使用Prettier 你可以在你书写的时候自动格式化代码以保证项目的整体风格。查看 [Prettier's GitHub page][125] 以获取更多信息, 还有 [page to see it in action][126].

当我们在git中提交提交时，要格式化我们的代码，我们需要安装以下依赖项:

```sh
npm install --save husky lint-staged prettier
```

或者你可以使用 `yarn`:

```sh
yarn add husky lint-staged prettier
```

* `husky`让我们很容易就可以使用githooks，就好像它们是npm脚本一样。
* `lint-staged`允许我们在git中运行脚本文件. 查看 [关于 lint-staged的博客文章][127]来了解更多信息.
* `prettier` 是我们在提交之前运行的JavaScript格式化程序.

现在，我们可以通过向`package.json`中添加几行来确保每个文件都被格式化。

将下面几行添加到 `scripts`中:

```diff
  "scripts": {
+   "precommit": "lint-staged",
    "start": "react-scripts start",
    "build": "react-scripts build",
```

接下来我们添加 'lint-staged' 片段到 `package.json`,比如:

```diff
  "dependencies": {
    // ...
  },
+ "lint-staged": {
+   "src/**/*.{js,jsx,json,css}": [
+     "prettier --single-quote --write",
+     "git add"
+   ]
+ },
  "scripts": {
```

现在，当你提交一个提交时，Prettier会自动地格式化已修改的文件。 你可以运行 `./node_modules/.bin/prettier --single-quote --write "src/**/*.{js,jsx}"` 来对整个项目进行第一次格式化.

Next you might want to integrate Prettier in your favorite editor. Read the section on [Editor Integration][128] on the Prettier GitHub page 接下来，您可能希望在您最喜欢的编辑器中集成Prettier。在Prettier GitHub页面上阅读[Editor Integration][129]一节.

## Changing the Page `<title>`
改变页面的`<title>`
您可以在生成的项目的`public`文件夹中找到源HTML文件。你可以编辑标签中的`<title>`，将标题从“React App”更改为其他任何东西。

请注意，通常情况下，您不会经常在`public`中编辑文件。例如，[添加一个样式表][130]是在不涉及HTML的情况下完成的。

您需要根据内容动态更新页面标题，您可以使用浏览器[`document.title`][131] API。对于更复杂的场景，当您想要更改来自React组件的标题时，您可以使用[React Helmet][132]，一个第三方库。

如果您在生产中使用定制服务器，并希望在发送到浏览器之前修改标题，那么您可以在[这一节][133]中遵循建议。或者，您可以将每个页面预先构建为一个静态HTML文件，然后加载JavaScript包，[这里][134]已经介绍了。

## Installing a Dependency
安装依赖
生成的项目包括作为依赖项的React和ReactDOM。它还包括一组用于Create React App作为开发依赖的脚本。您还可以使用`npm`安装其他依赖项(例如，响应路由器):

```sh
npm install --save react-router
```

你还可以使用 `yarn`:

```sh
yarn add react-router
```

它适用于任何库，而不仅仅是 `react-router`.

## Importing a Component
导入组件
这个项目设置支持ES6模块，这样感谢Babel.<br>
你仍然可以使用 `require()` 和 `module.exports`, 我们推荐使用 [`import` 和`export`][135] instead.

例如:

### `Button.js`

```js
import React, { Component } from 'react';

class Button extends Component {
  render() {
    // ...
  }
}

export default Button; // Don’t forget to use export default!
```

### `DangerButton.js`


```js
import React, { Component } from 'react';
import Button from './Button'; // Import a component from another file

class DangerButton extends Component {
  render() {
    return <Button color="red" />;
  }
}

export default DangerButton;
```

请注意 [默认和命名导出的区别][136]. 这是一个常见的错误来源.


我们建议，当一个模块只导出一个东西(例如，一个组件)时，您将坚持使用默认的导入和导出。这就是当你使用`export default Button` and `import Button from './Button'`所得到的结果。

 命名导出对于导出几个函数的实用程序模块非常有用。一个模块*最多可能有一个默认的导出*，以及您所喜欢的许多命名导出。

了解更多关于ES6模块的信息:

* [ 什么时候用大括号?][137]
* [ 探索ES6:模块 ][138]
* [ 理解ES6:模块 ][139]

## Code Splitting
代码分割
在用户可以使用之前，先不要下载整个应用程序，而代码分裂则允许你将代码分成小块，然后按需加载。

这个项目设置支持通过[动态 `import()`][140]进行代码分割。它的[建议][141]在第三阶段。`import()`函数式表单以模块名作为参数，并返回一个始终解析模块名称空间对象的[`Promise`][142]。

例如:

### `moduleA.js`

```js
const moduleA = 'Hello';

export { moduleA };
```
### `App.js`

```js
import React, { Component } from 'react';

class App extends Component {
  handleClick = () => {
    import('./moduleA')
      .then(({ moduleA }) => {
        // Use moduleA
      })
      .catch(err => {
        // Handle failure
      });
  };

  render() {
    return (
      <div>
        <button onClick={this.handleClick}>Load</button>
      </div>
    );
  }
}

export default App;
```

This will make `moduleA.js` and all its unique dependencies as a separate chunk that only loads after the user clicks the 'Load' button.

You can also use it with ` syntax if you prefer it.
`这将使`moduleA.js`及其所有独特的依赖项作为单独的块，只有在用户点击“Load”按钮后才会加载。

如果您愿意，也可以使用`async` / `await`语法

### With React Router
React路由
If you are using React Router check out  on how to use code splitting with it. You can find the companion GitHub repository  如果您正在使用React Router，请参阅[ 本教程 ][143]，了解如何使用代码与之分离。您可以在这里[这里][144] 找到GitHub的GitHub库.

## Adding a Stylesheet

This project setup uses [Webpack][145] for handling all assets. Webpack offers a custom way of “extending” the concept of `import` beyond JavaScript. To express that a JavaScript file depends on a CSS file, you need to **import the CSS from the JavaScript file**:

### `Button.css`

```css
.Button {
  padding: 20px;
}
```

### `Button.js`

```js
import React, { Component } from 'react';
import './Button.css'; // Tell Webpack that Button.js uses these styles

class Button extends Component {
  render() {
    // You can use them as regular CSS styles
    return <div className="Button" />;
  }
}
```

**This is not required for React** but many people find this feature convenient. You can read about the benefits of this approach [here][146]. However you should be aware that this makes your code less portable to other build tools and environments than Webpack.

In development, expressing dependencies this way allows your styles to be reloaded on the fly as you edit them. In production, all CSS files will be concatenated into a single minified `.css` file in the build output.

If you are concerned about using Webpack-specific semantics, you can put all your CSS right into `src/index.css`. It would still be imported from `src/index.js`, but you could always remove that import if you later migrate to a different build tool.

## Post-Processing CSS

This project setup minifies your CSS and adds vendor prefixes to it automatically through [Autoprefixer][147] so you don’t need to worry about it.

For example, this:

```css
.App {
  display: flex;
  flex-direction: row;
  align-items: center;
}
```

becomes this:

```css
.App {
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-orient: horizontal;
  -webkit-box-direction: normal;
      -ms-flex-direction: row;
          flex-direction: row;
  -webkit-box-align: center;
      -ms-flex-align: center;
          align-items: center;
}
```

If you need to disable autoprefixing for some reason, [follow this section][148].

## Adding a CSS Preprocessor (Sass, Less etc.)

Generally, we recommend that you don’t reuse the same CSS classes across different components. For example, instead of using a `.Button` CSS class in `<AcceptButton>` and `<RejectButton>` components, we recommend creating a `<Button>` component with its own `.Button` styles, that both `<AcceptButton>` and `<RejectButton>` can render (but [not inherit][149]).

Following this rule often makes CSS preprocessors less useful, as features like mixins and nesting are replaced by component composition. You can, however, integrate a CSS preprocessor if you find it valuable. In this walkthrough, we will be using Sass, but you can also use Less, or another alternative.

First, let’s install the command-line interface for Sass:

```sh
npm install --save node-sass-chokidar
```

Alternatively you may use `yarn`:

```sh
yarn add node-sass-chokidar
```

Then in `package.json`, add the following lines to `scripts`:

```diff
   "scripts": {
+    "build-css": "node-sass-chokidar src/ -o src/",
+    "watch-css": "npm run build-css && node-sass-chokidar src/ -o src/ --watch --recursive",
     "start": "react-scripts start",
     "build": "react-scripts build",
     "test": "react-scripts test --env=jsdom",
```

> Note: To use a different preprocessor, replace `build-css` and `watch-css` commands according to your preprocessor’s documentation.

Now you can rename `src/App.css` to `src/App.scss` and run `npm run watch-css`. The watcher will find every Sass file in `src` subdirectories, and create a corresponding CSS file next to it, in our case overwriting `src/App.css`. Since `src/App.js` still imports `src/App.css`, the styles become a part of your application. You can now edit `src/App.scss`, and `src/App.css` will be regenerated.

To share variables between Sass files, you can use Sass imports. For example, `src/App.scss` and other component style files could include `@import "./shared.scss";` with variable definitions.

To enable importing files without using relative paths, you can add the  `--include-path` option to the command in `package.json`.

```
"build-css": "node-sass-chokidar --include-path ./src --include-path ./node_modules src/ -o src/",
"watch-css": "npm run build-css && node-sass-chokidar --include-path ./src --include-path ./node_modules src/ -o src/ --watch --recursive",
```

This will allow you to do imports like

```scss
@import 'styles/_colors.scss'; // assuming a styles directory under src/
@import 'nprogress/nprogress'; // importing a css file from the nprogress node module
```

At this point you might want to remove all CSS files from the source control, and add `src/**/*.css` to your `.gitignore` file. It is generally a good practice to keep the build products outside of the source control.

As a final step, you may find it convenient to run `watch-css` automatically with `npm start`, and run `build-css` as a part of `npm run build`. You can use the `&&` operator to execute two scripts sequentially. However, there is no cross-platform way to run two scripts in parallel, so we will install a package for this:

```sh
npm install --save npm-run-all
```

Alternatively you may use `yarn`:

```sh
yarn add npm-run-all
```

Then we can change `start` and `build` scripts to include the CSS preprocessor commands:

```diff
   "scripts": {
     "build-css": "node-sass-chokidar src/ -o src/",
     "watch-css": "npm run build-css && node-sass-chokidar src/ -o src/ --watch --recursive",
-    "start": "react-scripts start",
-    "build": "react-scripts build",
+    "start-js": "react-scripts start",
+    "start": "npm-run-all -p watch-css start-js",
+    "build": "npm run build-css && react-scripts build",
     "test": "react-scripts test --env=jsdom",
     "eject": "react-scripts eject"
   }
```

Now running `npm start` and `npm run build` also builds Sass files.

**Why `node-sass-chokidar`?**

`node-sass` has been reported as having the following issues:

- `node-sass --watch` has been reported to have *performance issues* in certain conditions when used in a virtual machine or with docker.

- Infinite styles compiling [^1939](https://github.com/facebookincubator/create-react-app/issues/1939)

- `node-sass` has been reported as having issues with detecting new files in a directory [^1891](https://github.com/sass/node-sass/issues/1891)

 `node-sass-chokidar` is used here as it addresses these issues.

## Adding Images, Fonts, and Files

With Webpack, using static assets like images and fonts works similarly to CSS.

You can **`import` a file right in a JavaScript module**. This tells Webpack to include that file in the bundle. Unlike CSS imports, importing a file gives you a string value. This value is the final path you can reference in your code, e.g. as the `src` attribute of an image or the `href` of a link to a PDF.

To reduce the number of requests to the server, importing images that are less than 10,000 bytes returns a [data URI][150] instead of a path. This applies to the following file extensions: bmp, gif, jpg, jpeg, and png. SVG files are excluded due to [^1153](https://github.com/facebookincubator/create-react-app/issues/1153).

Here is an example:

```js
import React from 'react';
import logo from './logo.png'; // Tell Webpack this JS file uses this image

console.log(logo); // /logo.84287d09.png

function Header() {
  // Import result is the URL of your image
  return <img src={logo} alt="Logo" />;
}

export default Header;
```

This ensures that when the project is built, Webpack will correctly move the images into the build folder, and provide us with correct paths.

This works in CSS too:

```css
.Logo {
  background-image: url(./logo.png);
}
```

Webpack finds all relative module references in CSS (they start with `./`) and replaces them with the final paths from the compiled bundle. If you make a typo or accidentally delete an important file, you will see a compilation error, just like when you import a non-existent JavaScript module. The final filenames in the compiled bundle are generated by Webpack from content hashes. If the file content changes in the future, Webpack will give it a different name in production so you don’t need to worry about long-term caching of assets.

Please be advised that this is also a custom feature of Webpack.

**It is not required for React** but many people enjoy it (and React Native uses a similar mechanism for images).<br>
An alternative way of handling static assets is described in the next section.

## Using the `public` Folder

> Note: this feature is available with `react-scripts@0.5.0` and higher.

### Changing the HTML

The `public` folder contains the HTML file so you can tweak it, for example, to [set the page title][151].
The `<script>` tag with the compiled code will be added to it automatically during the build process.

### Adding Assets Outside of the Module System

You can also add other assets to the `public` folder.

Note that we normally encourage you to `import` assets in JavaScript files instead.
For example, see the sections on [adding a stylesheet][152] and [adding images and fonts][153].
This mechanism provides a number of benefits:

* Scripts and stylesheets get minified and bundled together to avoid extra network requests.
* Missing files cause compilation errors instead of 404 errors for your users.
* Result filenames include content hashes so you don’t need to worry about browsers caching their old versions.

However there is an **escape hatch** that you can use to add an asset outside of the module system.

If you put a file into the `public` folder, it will **not** be processed by Webpack. Instead it will be copied into the build folder untouched.   To reference assets in the `public` folder, you need to use a special variable called `PUBLIC_URL`.

Inside `index.html`, you can use it like this:

```html
<link rel="shortcut icon" href="%PUBLIC_URL%/favicon.ico">
```

Only files inside the `public` folder will be accessible by `%PUBLIC_URL%` prefix. If you need to use a file from `src` or `node_modules`, you’ll have to copy it there to explicitly specify your intention to make this file a part of the build.

When you run `npm run build`, Create React App will substitute `%PUBLIC_URL%` with a correct absolute path so your project works even if you use client-side routing or host it at a non-root URL.

In JavaScript code, you can use `process.env.PUBLIC_URL` for similar purposes:

```js
render() {
  // Note: this is an escape hatch and should be used sparingly!
  // Normally we recommend using `import` for getting asset URLs
  // as described in “Adding Images and Fonts” above this section.
  return <img src={process.env.PUBLIC_URL + '/img/logo.png'} />;
}
```

Keep in mind the downsides of this approach:

* None of the files in `public` folder get post-processed or minified.
* Missing files will not be called at compilation time, and will cause 404 errors for your users.
* Result filenames won’t include content hashes so you’ll need to add query arguments or rename them every time they change.

### When to Use the `public` Folder

Normally we recommend importing [stylesheets][154], [images, and fonts][155] from JavaScript.
The `public` folder is useful as a workaround for a number of less common cases:

* You need a file with a specific name in the build output, such as [`manifest.webmanifest`][156].
* You have thousands of images and need to dynamically reference their paths.
* You want to include a small script like [`pace.js`][157] outside of the bundled code.
* Some library may be incompatible with Webpack and you have no other option but to include it as a `<script>` tag.

Note that if you add a `<script>` that declares global variables, you also need to read the next section on using them.

## Using Global Variables

When you include a script in the HTML file that defines global variables and try to use one of these variables in the code, the linter will complain because it cannot see the definition of the variable.

You can avoid this by reading the global variable explicitly from the `window` object, for example:

```js
const $ = window.$;
```

This makes it obvious you are using a global variable intentionally rather than because of a typo.

Alternatively, you can force the linter to ignore any line by adding `// eslint-disable-line` after it.

## Adding Bootstrap

You don’t have to use [React Bootstrap][158] together with React but it is a popular library for integrating Bootstrap with React apps. If you need it, you can integrate it with Create React App by following these steps:

Install React Bootstrap and Bootstrap from npm. React Bootstrap does not include Bootstrap CSS so this needs to be installed as well:

```sh
npm install --save react-bootstrap bootstrap@3
```

Alternatively you may use `yarn`:

```sh
yarn add react-bootstrap bootstrap@3
```

Import Bootstrap CSS and optionally Bootstrap theme CSS in the beginning of your `src/index.js` file:

```js
import 'bootstrap/dist/css/bootstrap.css';
import 'bootstrap/dist/css/bootstrap-theme.css';
// Put any other imports below so that CSS from your
// components takes precedence over default styles.
```

Import required React Bootstrap components within `src/App.js` file or your custom component files:

```js
import { Navbar, Jumbotron, Button } from 'react-bootstrap';
```

Now you are ready to use the imported React Bootstrap components within your component hierarchy defined in the render method. Here is an example [`App.js`][159] redone using React Bootstrap.

### Using a Custom Theme

Sometimes you might need to tweak the visual styles of Bootstrap (or equivalent package).<br>
We suggest the following approach:

* Create a new package that depends on the package you wish to customize, e.g. Bootstrap.
* Add the necessary build steps to tweak the theme, and publish your package on npm.
* Install your own theme npm package as a dependency of your app.

Here is an example of adding a [customized Bootstrap][160] that follows these steps.

## Adding Flow

Flow is a static type checker that helps you write code with fewer bugs. Check out this [introduction to using static types in JavaScript][161] if you are new to this concept.

Recent versions of [Flow][162] work with Create React App projects out of the box.

To add Flow to a Create React App project, follow these steps:

1. Run `npm install --save flow-bin` (or `yarn add flow-bin`).
2. Add `"flow": "flow"` to the `scripts` section of your `package.json`.
3. Run `npm run flow init` (or `yarn flow init`) to create a [`.flowconfig` file][163] in the root directory.
4. Add `// @flow` to any files you want to type check (for example, to `src/App.js`).

Now you can run `npm run flow` (or `yarn flow`) to check the files for type errors.
You can optionally use an IDE like [Nuclide][164] for a better integrated experience.
In the future we plan to integrate it into Create React App even more closely.

To learn more about Flow, check out [its documentation][165].

## Adding Custom Environment Variables

> Note: this feature is available with `react-scripts@0.2.3` and higher.

Your project can consume variables declared in your environment as if they were declared locally in your JS files. By
default you will have `NODE_ENV` defined for you, and any other environment variables starting with
`REACT_APP_`.

**The environment variables are embedded during the build time**. Since Create React App produces a static HTML/CSS/JS bundle, it can’t possibly read them at runtime. To read them at runtime, you would need to load HTML into memory on the server and replace placeholders in runtime, just like [described here][166]. Alternatively you can rebuild the app on the server anytime you change them.

> Note: You must create custom environment variables beginning with `REACT_APP_`. Any other variables except `NODE_ENV` will be ignored to avoid accidentally [exposing a private key on the machine that could have the same name][167]. Changing any environment variables will require you to restart the development server if it is running.

These environment variables will be defined for you on `process.env`. For example, having an environment
variable named `REACT_APP_SECRET_CODE` will be exposed in your JS as `process.env.REACT_APP_SECRET_CODE`.

There is also a special built-in environment variable called `NODE_ENV`. You can read it from `process.env.NODE_ENV`. When you run `npm start`, it is always equal to `'development'`, when you run `npm test` it is always equal to `'test'`, and when you run `npm run build` to make a production bundle, it is always equal to `'production'`. **You cannot override `NODE_ENV` manually.** This prevents developers from accidentally deploying a slow development build to production.

These environment variables can be useful for displaying information conditionally based on where the project is
deployed or consuming sensitive data that lives outside of version control.

First, you need to have environment variables defined. For example, let’s say you wanted to consume a secret defined
in the environment inside a `<form>`:

```jsx
render() {
  return (
    <div>
      <small>You are running this application in <b>{process.env.NODE_ENV}</b> mode.</small>
      <form>
        <input type="hidden" defaultValue={process.env.REACT_APP_SECRET_CODE} />
      </form>
    </div>
  );
}
```

During the build, `process.env.REACT_APP_SECRET_CODE` will be replaced with the current value of the `REACT_APP_SECRET_CODE` environment variable. Remember that the `NODE_ENV` variable will be set for you automatically.

When you load the app in the browser and inspect the `<input>`, you will see its value set to `abcdef`, and the bold text will show the environment provided when using `npm start`:

```html
<div>
  <small>You are running this application in <b>development</b> mode.</small>
  <form>
    <input type="hidden" value="abcdef" />
  </form>
</div>
```

The above form is looking for a variable called `REACT_APP_SECRET_CODE` from the environment. In order to consume this
value, we need to have it defined in the environment. This can be done using two ways: either in your shell or in
a `.env` file. Both of these ways are described in the next few sections.

Having access to the `NODE_ENV` is also useful for performing actions conditionally:

```js
if (process.env.NODE_ENV !== 'production') {
  analytics.disable();
}
```

When you compile the app with `npm run build`, the minification step will strip out this condition, and the resulting bundle will be smaller.

### Referencing Environment Variables in the HTML

> Note: this feature is available with `react-scripts@0.9.0` and higher.

You can also access the environment variables starting with `REACT_APP_` in the `public/index.html`. For example:

```html
<title>%REACT_APP_WEBSITE_NAME%</title>
```

Note that the caveats from the above section apply:

* Apart from a few built-in variables (`NODE_ENV` and `PUBLIC_URL`), variable names must start with `REACT_APP_` to work.
* The environment variables are injected at build time. If you need to inject them at runtime, [follow this approach instead][168].

### Adding Temporary Environment Variables In Your Shell

Defining environment variables can vary between OSes. It’s also important to know that this manner is temporary for the
life of the shell session.

#### Windows (cmd.exe)

```cmd
set REACT_APP_SECRET_CODE=abcdef&&npm start
```

(Note: the lack of whitespace is intentional.)

#### Linux, macOS (Bash)

```bash
REACT_APP_SECRET_CODE=abcdef npm start
```

### Adding Development Environment Variables In `.env`

> Note: this feature is available with `react-scripts@0.5.0` and higher.

To define permanent environment variables, create a file called `.env` in the root of your project:

```
REACT_APP_SECRET_CODE=abcdef
```

`.env` files **should be** checked into source control (with the exclusion of `.env*.local`).

#### What other `.env` files are can be used?

> Note: this feature is **available with `react-scripts@1.0.0` and higher**.

* `.env`: Default.
* `.env.local`: Local overrides. **This file is loaded for all environments except test.**
* `.env.development`, `.env.test`, `.env.production`: Environment-specific settings.
* `.env.development.local`, `.env.test.local`, `.env.production.local`: Local overrides of environment-specific settings.

Files on the left have more priority than files on the right:

* `npm start`: `.env.development.local`, `.env.development`, `.env.local`, `.env`
* `npm run build`: `.env.production.local`, `.env.production`, `.env.local`, `.env`
* `npm test`: `.env.test.local`, `.env.test`, `.env` (note `.env.local` is missing)

These variables will act as the defaults if the machine does not explicitly set them.<br>
Please refer to the [dotenv documentation][169] for more details.

> Note: If you are defining environment variables for development, your CI and/or hosting platform will most likely need
these defined as well. Consult their documentation how to do this. For example, see the documentation for [Travis CI][170] or [Heroku][171].

## Can I Use Decorators?

Many popular libraries use [decorators][172] in their documentation.<br>
Create React App doesn’t support decorator syntax at the moment because:

* It is an experimental proposal and is subject to change.
* The current specification version is not officially supported by Babel.
* If the specification changes, we won’t be able to write a codemod because we don’t use them internally at Facebook.

However in many cases you can rewrite decorator-based code without decorators just as fine.<br>
Please refer to these two threads for reference:

* [^214](https://github.com/facebookincubator/create-react-app/issues/214)
* [^411](https://github.com/facebookincubator/create-react-app/issues/411)

Create React App will add decorator support when the specification advances to a stable stage.

## Integrating with an API Backend

These tutorials will help you to integrate your app with an API backend running on another port,
using `fetch()` to access it.

### Node
Check out [this tutorial][173].
You can find the companion GitHub repository [here][174].

### Ruby on Rails

Check out [this tutorial][175].
You can find the companion GitHub repository [here][176].

## Proxying API Requests in Development

> Note: this feature is available with `react-scripts@0.2.3` and higher.

People often serve the front-end React app from the same host and port as their backend implementation.<br>
For example, a production setup might look like this after the app is deployed:

```
/             - static server returns index.html with React app
/todos        - static server returns index.html with React app
/api/todos    - server handles any /api/* requests using the backend implementation
```

Such setup is **not** required. However, if you **do** have a setup like this, it is convenient to write requests like `fetch('/api/todos')` without worrying about redirecting them to another host or port during development.

To tell the development server to proxy any unknown requests to your API server in development, add a `proxy` field to your `package.json`, for example:

```js
  "proxy": "http://localhost:4000",
```

This way, when you `fetch('/api/todos')` in development, the development server will recognize that it’s not a static asset, and will proxy your request to `http://localhost:4000/api/todos` as a fallback. The development server will **only** attempt to send requests without `text/html` in its `Accept` header to the proxy.

Conveniently, this avoids [CORS issues][177] and error messages like this in development:

```
Fetch API cannot load http://localhost:4000/api/todos. No 'Access-Control-Allow-Origin' header is present on the requested resource. Origin 'http://localhost:3000' is therefore not allowed access. If an opaque response serves your needs, set the request's mode to 'no-cors' to fetch the resource with CORS disabled.
```

Keep in mind that `proxy` only has effect in development (with `npm start`), and it is up to you to ensure that URLs like `/api/todos` point to the right thing in production. You don’t have to use the `/api` prefix. Any unrecognized request without a `text/html` accept header will be redirected to the specified `proxy`.

The `proxy` option supports HTTP, HTTPS and WebSocket connections.<br>
If the `proxy` option is **not** flexible enough for you, alternatively you can:

* [Configure the proxy yourself][178]
* Enable CORS on your server ([here’s how to do it for Express][179]).
* Use [environment variables][180] to inject the right server host and port into your app.

### "Invalid Host Header" Errors After Configuring Proxy

When you enable the `proxy` option, you opt into a more strict set of host checks. This is necessary because leaving the backend open to remote hosts makes your computer vulnerable to DNS rebinding attacks. The issue is explained in [this article][181] and [this issue][182].

This shouldn’t affect you when developing on `localhost`, but if you develop remotely like [described here][183], you will see this error in the browser after enabling the `proxy` option:

> Invalid Host header

To work around it, you can specify your public development host in a file called `.env.development` in the root of your project:

```
HOST=mypublicdevhost.com
```

If you restart the development server now and load the app from the specified host, it should work.

If you are still having issues or if you’re using a more exotic environment like a cloud editor, you can bypass the host check completely by adding a line to `.env.development.local`. **Note that this is dangerous and exposes your machine to remote code execution from malicious websites:**

```
# NOTE: THIS IS DANGEROUS!
# It exposes your machine to attacks from the websites you visit.
DANGEROUSLY_DISABLE_HOST_CHECK=true
```

We don’t recommend this approach.

### Configuring the Proxy Manually

> Note: this feature is available with `react-scripts@1.0.0` and higher.

If the `proxy` option is **not** flexible enough for you, you can specify an object in the following form (in `package.json`).<br>
You may also specify any configuration value [`http-proxy-middleware`][184] or [`http-proxy`][185] supports.
```js
{
  // ...
  "proxy": {
    "/api": {
      "target": "<url>",
      "ws": true
      // ...
    }
  }
  // ...
}
```

All requests matching this path will be proxies, no exceptions. This includes requests for `text/html`, which the standard `proxy` option does not proxy.

If you need to specify multiple proxies, you may do so by specifying additional entries.
Matches are regular expressions, so that you can use a regexp to match multiple paths.
```js
{
  // ...
  "proxy": {
    // Matches any request starting with /api
    "/api": {
      "target": "<url_1>",
      "ws": true
      // ...
    },
    // Matches any request starting with /foo
    "/foo": {
      "target": "<url_2>",
      "ssl": true,
      "pathRewrite": {
        "^/foo": "/foo/beta"
      }
      // ...
    },
    // Matches /bar/abc.html but not /bar/sub/def.html
    "/bar/[^/]*[.]html": {
      "target": "<url_3>",
      // ...
    },
    // Matches /baz/abc.html and /baz/sub/def.html
    "/baz/.*/.*[.]html": {
      "target": "<url_4>"
      // ...
    }
  }
  // ...
}
```

### Configuring a WebSocket Proxy

When setting up a WebSocket proxy, there are a some extra considerations to be aware of.

If you’re using a WebSocket engine like [Socket.io][186], you must have a Socket.io server running that you can use as the proxy target. Socket.io will not work with a standard WebSocket server. Specifically, don't expect Socket.io to work with [the websocket.org echo test][187].

There’s some good documentation available for [setting up a Socket.io server][188].

Standard WebSockets **will** work with a standard WebSocket server as well as the websocket.org echo test. You can use libraries like [ws][189] for the server, with [native WebSockets in the browser][190].

Either way, you can proxy WebSocket requests manually in `package.json`:

```js
{
  // ...
  "proxy": {
    "/socket": {
      // Your compatible WebSocket server
      "target": "ws://<socket_url>",
      // Tell http-proxy-middleware that this is a WebSocket proxy.
      // Also allows you to proxy WebSocket requests without an additional HTTP request
      // https://github.com/chimurai/http-proxy-middleware#external-websocket-upgrade
      "ws": true
      // ...
    }
  }
  // ...
}
```

## Using HTTPS in Development

> Note: this feature is available with `react-scripts@0.4.0` and higher.

You may require the dev server to serve pages over HTTPS. One particular case where this could be useful is when using [the "proxy" feature][191] to proxy requests to an API server when that API server is itself serving HTTPS.

To do this, set the `HTTPS` environment variable to `true`, then start the dev server as usual with `npm start`:

#### Windows (cmd.exe)

```cmd
set HTTPS=true&&npm start
```

(Note: the lack of whitespace is intentional.)

#### Linux, macOS (Bash)

```bash
HTTPS=true npm start
```

Note that the server will use a self-signed certificate, so your web browser will almost definitely display a warning upon accessing the page.

## Generating Dynamic `<meta>` Tags on the Server

Since Create React App doesn’t support server rendering, you might be wondering how to make `<meta>` tags dynamic and reflect the current URL. To solve this, we recommend to add placeholders into the HTML, like this:

```html
<!doctype html>
<html lang="en">
  <head>
    <meta property="og:title" content="__OG_TITLE__">
    <meta property="og:description" content="__OG_DESCRIPTION__">
```

Then, on the server, regardless of the backend you use, you can read `index.html` into memory and replace `__OG_TITLE__`, `__OG_DESCRIPTION__`, and any other placeholders with values depending on the current URL. Just make sure to sanitize and escape the interpolated values so that they are safe to embed into HTML!

If you use a Node server, you can even share the route matching logic between the client and the server. However duplicating it also works fine in simple cases.

## Pre-Rendering into Static HTML Files

If you’re hosting your `build` with a static hosting provider you can use [react-snapshot][192] to generate HTML pages for each route, or relative link, in your application. These pages will then seamlessly become active, or “hydrated”, when the JavaScript bundle has loaded.

There are also opportunities to use this outside of static hosting, to take the pressure off the server when generating and caching routes.

The primary benefit of pre-rendering is that you get the core content of each page _with_ the HTML payload—regardless of whether or not your JavaScript bundle successfully downloads. It also increases the likelihood that each route of your application will be picked up by search engines.

You can read more about [zero-configuration pre-rendering (also called snapshotting) here][193].

## Injecting Data from the Server into the Page

Similarly to the previous section, you can leave some placeholders in the HTML that inject global variables, for example:

```js
<!doctype html>
<html lang="en">
  <head>
    <script>
      window.SERVER_DATA = __SERVER_DATA__;
    </script>
```

Then, on the server, you can replace `__SERVER_DATA__` with a JSON of real data right before sending the response. The client code can then read `window.SERVER_DATA` to use it. **Make sure to [sanitize the JSON before sending it to the client][194] as it makes your app vulnerable to XSS attacks.**

## Running Tests

> Note: this feature is available with `react-scripts@0.3.0` and higher.<br>
> [Read the migration guide to learn how to enable it in older projects!][195]

Create React App uses [Jest][196] as its test runner. To prepare for this integration, we did a [major revamp][197] of Jest so if you heard bad things about it years ago, give it another try.

Jest is a Node-based runner. This means that the tests always run in a Node environment and not in a real browser. This lets us enable fast iteration speed and prevent flakiness.

While Jest provides browser globals such as `window` thanks to [jsdom][198], they are only approximations of the real browser behavior. Jest is intended to be used for unit tests of your logic and your components rather than the DOM quirks.

We recommend that you use a separate tool for browser end-to-end tests if you need them. They are beyond the scope of Create React App.

### Filename Conventions

Jest will look for test files with any of the following popular naming conventions:

* Files with `.js` suffix in `__tests__` folders.
* Files with `.test.js` suffix.
* Files with `.spec.js` suffix.

The `.test.js` / `.spec.js` files (or the `__tests__` folders) can be located at any depth under the `src` top level folder.

We recommend to put the test files (or `__tests__` folders) next to the code they are testing so that relative imports appear shorter. For example, if `App.test.js` and `App.js` are in the same folder, the test just needs to `import App from './App'` instead of a long relative path. Colocation also helps find tests more quickly in larger projects.

### Command Line Interface

When you run `npm test`, Jest will launch in the watch mode. Every time you save a file, it will re-run the tests, just like `npm start` recompiles the code.

The watcher includes an interactive command-line interface with the ability to run all tests, or focus on a search pattern. It is designed this way so that you can keep it open and enjoy fast re-runs. You can learn the commands from the “Watch Usage” note that the watcher prints after every run:

![Jest watch mode][image-1]

### Version Control Integration

By default, when you run `npm test`, Jest will only run the tests related to files changed since the last commit. This is an optimization designed to make your tests run fast regardless of how many tests you have. However it assumes that you don’t often commit the code that doesn’t pass the tests.

Jest will always explicitly mention that it only ran tests related to the files changed since the last commit. You can also press `a` in the watch mode to force Jest to run all tests.

Jest will always run all tests on a [continuous integration][199] server or if the project is not inside a Git or Mercurial repository.

### Writing Tests

To create tests, add `it()` (or `test()`) blocks with the name of the test and its code. You may optionally wrap them in `describe()` blocks for logical grouping but this is neither required nor recommended.

Jest provides a built-in `expect()` global function for making assertions. A basic test could look like this:

```js
import sum from './sum';

it('sums numbers', () => {
  expect(sum(1, 2)).toEqual(3);
  expect(sum(2, 2)).toEqual(4);
});
```

All `expect()` matchers supported by Jest are [extensively documented here][200].<br>
You can also use [`jest.fn()` and `expect(fn).toBeCalled()`][201] to create “spies” or mock functions.

### Testing Components

There is a broad spectrum of component testing techniques. They range from a “smoke test” verifying that a component renders without throwing, to shallow rendering and testing some of the output, to full rendering and testing component lifecycle and state changes.

Different projects choose different testing tradeoffs based on how often components change, and how much logic they contain. If you haven’t decided on a testing strategy yet, we recommend that you start with creating simple smoke tests for your components:

```js
import React from 'react';
import ReactDOM from 'react-dom';
import App from './App';

it('renders without crashing', () => {
  const div = document.createElement('div');
  ReactDOM.render(<App />, div);
});
```

This test mounts a component and makes sure that it didn’t throw during rendering. Tests like this provide a lot value with very little effort so they are great as a starting point, and this is the test you will find in `src/App.test.js`.

When you encounter bugs caused by changing components, you will gain a deeper insight into which parts of them are worth testing in your application. This might be a good time to introduce more specific tests asserting specific expected output or behavior.

If you’d like to test components in isolation from the child components they render, we recommend using [`shallow()` rendering API][202] from [Enzyme][203]. To install it, run:

```sh
npm install --save enzyme react-test-renderer
```

Alternatively you may use `yarn`:

```sh
yarn add enzyme react-test-renderer
```

You can write a smoke test with it too:

```js
import React from 'react';
import { shallow } from 'enzyme';
import App from './App';

it('renders without crashing', () => {
  shallow(<App />);
});
```

Unlike the previous smoke test using `ReactDOM.render()`, this test only renders `<App>` and doesn’t go deeper. For example, even if `<App>` itself renders a `<Button>` that throws, this test will pass. Shallow rendering is great for isolated unit tests, but you may still want to create some full rendering tests to ensure the components integrate correctly. Enzyme supports [full rendering with `mount()`][204], and you can also use it for testing state changes and component lifecycle.

You can read the [Enzyme documentation][205] for more testing techniques. Enzyme documentation uses Chai and Sinon for assertions but you don’t have to use them because Jest provides built-in `expect()` and `jest.fn()` for spies.

Here is an example from Enzyme documentation that asserts specific output, rewritten to use Jest matchers:

```js
import React from 'react';
import { shallow } from 'enzyme';
import App from './App';

it('renders welcome message', () => {
  const wrapper = shallow(<App />);
  const welcome = <h2>Welcome to React</h2>;
  // expect(wrapper.contains(welcome)).to.equal(true);
  expect(wrapper.contains(welcome)).toEqual(true);
});
```

All Jest matchers are [extensively documented here][206].<br>
Nevertheless you can use a third-party assertion library like [Chai][207] if you want to, as described below.

Additionally, you might find [jest-enzyme][208] helpful to simplify your tests with readable matchers. The above `contains` code can be written simpler with jest-enzyme.

```js
expect(wrapper).toContainReact(welcome)
```

To enable this, install `jest-enzyme`:

```sh
npm install --save jest-enzyme
```

Alternatively you may use `yarn`:

```sh
yarn add jest-enzyme
```

Import it in [`src/setupTests.js`][209] to make its matchers available in every test:

```js
import 'jest-enzyme';
```

### Using Third Party Assertion Libraries

We recommend that you use `expect()` for assertions and `jest.fn()` for spies. If you are having issues with them please [file those against Jest][210], and we’ll fix them. We intend to keep making them better for React, supporting, for example, [pretty-printing React elements as JSX][211].

However, if you are used to other libraries, such as [Chai][212] and [Sinon][213], or if you have existing code using them that you’d like to port over, you can import them normally like this:

```js
import sinon from 'sinon';
import { expect } from 'chai';
```

and then use them in your tests like you normally do.

### Initializing Test Environment

> Note: this feature is available with `react-scripts@0.4.0` and higher.

If your app uses a browser API that you need to mock in your tests or if you just need a global setup before running your tests, add a `src/setupTests.js` to your project. It will be automatically executed before running your tests.

For example:

#### `src/setupTests.js`
```js
const localStorageMock = {
  getItem: jest.fn(),
  setItem: jest.fn(),
  clear: jest.fn()
};
global.localStorage = localStorageMock
```

### Focusing and Excluding Tests

You can replace `it()` with `xit()` to temporarily exclude a test from being executed.<br>
Similarly, `fit()` lets you focus on a specific test without running any other tests.

### Coverage Reporting

Jest has an integrated coverage reporter that works well with ES6 and requires no configuration.<br>
Run `npm test -- --coverage` (note extra `--` in the middle) to include a coverage report like this:

![coverage report][image-2]

Note that tests run much slower with coverage so it is recommended to run it separately from your normal workflow.

### Continuous Integration

By default `npm test` runs the watcher with interactive CLI. However, you can force it to run tests once and finish the process by setting an environment variable called `CI`.

When creating a build of your application with `npm run build` linter warnings are not checked by default. Like `npm test`, you can force the build to perform a linter warning check by setting the environment variable `CI`. If any warnings are encountered then the build fails.

Popular CI servers already set the environment variable `CI` by default but you can do this yourself too:

### On CI servers
#### Travis CI

1. Following the [Travis Getting started][214] guide for syncing your GitHub repository with Travis.  You may need to initialize some settings manually in your [profile][215] page.
1. Add a `.travis.yml` file to your git repository.
```
language: node_js
node_js:
  - 6
cache:
  directories:
    - node_modules
script:
  - npm run build
  - npm test
```
1. Trigger your first build with a git push.
1. [Customize your Travis CI Build][216] if needed.

#### CircleCI

Follow [this article][217] to set up CircleCI with a Create React App project.

### On your own environment
##### Windows (cmd.exe)

```cmd
set CI=true&&npm test
```

```cmd
set CI=true&&npm run build
```

(Note: the lack of whitespace is intentional.)

##### Linux, macOS (Bash)

```bash
CI=true npm test
```

```bash
CI=true npm run build
```

The test command will force Jest to run tests once instead of launching the watcher.

>  If you find yourself doing this often in development, please [file an issue][218] to tell us about your use case because we want to make watcher the best experience and are open to changing how it works to accommodate more workflows.

The build command will check for linter warnings and fail if any are found.

### Disabling jsdom

By default, the `package.json` of the generated project looks like this:

```js
  "scripts": {
    "start": "react-scripts start",
    "build": "react-scripts build",
    "test": "react-scripts test --env=jsdom"
```

If you know that none of your tests depend on [jsdom][219], you can safely remove `--env=jsdom`, and your tests will run faster:

```diff
  "scripts": {
    "start": "react-scripts start",
    "build": "react-scripts build",
-   "test": "react-scripts test --env=jsdom"
+   "test": "react-scripts test"
```

To help you make up your mind, here is a list of APIs that **need jsdom**:

* Any browser globals like `window` and `document`
* [`ReactDOM.render()`][220]
* [`TestUtils.renderIntoDocument()`][221] ([a shortcut][222] for the above)
* [`mount()`][223] in [Enzyme][224]

In contrast, **jsdom is not needed** for the following APIs:

* [`TestUtils.createRenderer()`][225] (shallow rendering)
* [`shallow()`][226] in [Enzyme][227]

Finally, jsdom is also not needed for [snapshot testing][228].

### Snapshot Testing

Snapshot testing is a feature of Jest that automatically generates text snapshots of your components and saves them on the disk so if the UI output changes, you get notified without manually writing any assertions on the component output. [Read more about snapshot testing.][229]

### Editor Integration

If you use [Visual Studio Code][230], there is a [Jest extension][231] which works with Create React App out of the box. This provides a lot of IDE-like features while using a text editor: showing the status of a test run with potential fail messages inline, starting and stopping the watcher automatically, and offering one-click snapshot updates.

![VS Code Jest Preview][image-3]

## Developing Components in Isolation

Usually, in an app, you have a lot of UI components, and each of them has many different states.
For an example, a simple button component could have following states:

* In a regular state, with a text label.
* In the disabled mode.
* In a loading state.

Usually, it’s hard to see these states without running a sample app or some examples.

Create React App doesn’t include any tools for this by default, but you can easily add [Storybook for React][232] ([source][233]) or [React Styleguidist][234] ([source][235]) to your project. **These are third-party tools that let you develop components and see all their states in isolation from your app**.

![Storybook for React Demo][image-4]

You can also deploy your Storybook or style guide as a static app. This way, everyone in your team can view and review different states of UI components without starting a backend server or creating an account in your app.

### Getting Started with Storybook

Storybook is a development environment for React UI components. It allows you to browse a component library, view the different states of each component, and interactively develop and test components.

First, install the following npm package globally:

```sh
npm install -g @storybook/cli
```

Then, run the following command inside your app’s directory:

```sh
getstorybook
```

After that, follow the instructions on the screen.

Learn more about React Storybook:

* Screencast: [Getting Started with React Storybook][236]
* [GitHub Repo][237]
* [Documentation][238]
* [Snapshot Testing UI][239] with Storybook + addon/storyshot

### Getting Started with Styleguidist

Styleguidist combines a style guide, where all your components are presented on a single page with their props documentation and usage examples, with an environment for developing components in isolation, similar to Storybook. In Styleguidist you write examples in Markdown, where each code snippet is rendered as a live editable playground.

First, install Styleguidist:

```sh
npm install --save react-styleguidist
```

Alternatively you may use `yarn`:

```sh
yarn add react-styleguidist
```

Then, add these scripts to your `package.json`:

```diff
   "scripts": {
+    "styleguide": "styleguidist server",
+    "styleguide:build": "styleguidist build",
     "start": "react-scripts start",
```

Then, run the following command inside your app’s directory:

```sh
npm run styleguide
```

After that, follow the instructions on the screen.

Learn more about React Styleguidist:

* [GitHub Repo][240]
* [Documentation][241]

## Making a Progressive Web App

By default, the production build is a fully functional, offline-first
[Progressive Web App][242].

Progressive Web Apps are faster and more reliable than traditional web pages, and provide an engaging mobile experience:

 * All static site assets are cached so that your page loads fast on subsequent visits, regardless of network connectivity (such as 2G or 3G). Updates are downloaded in the background.
 * Your app will work regardless of network state, even if offline. This means your users will be able to use your app at 10,000 feet and on the Subway.
 * On mobile devices, your app can be added directly to the user's home screen, app icon and all. You can also re-engage users using web **push notifications**. This eliminates the need for the app store.

The [`sw-precache-webpack-plugin`][243]
is integrated into production configuration,
and it will take care of generating a service worker file that will automatically
precache all of your local assets and keep them up to date as you deploy updates.
The service worker will use a [cache-first strategy][244]
for handling all requests for local assets, including the initial HTML, ensuring
that your web app is reliably fast, even on a slow or unreliable network.

### Opting Out of Caching

If you would prefer not to enable service workers prior to your initial
production deployment, then remove the call to `serviceWorkerRegistration.register()`
from [`src/index.js`][245].

If you had previously enabled service workers in your production deployment and
have decided that you would like to disable them for all your existing users,
you can swap out the call to `serviceWorkerRegistration.register()` in
[`src/index.js`][246] with a call to `serviceWorkerRegistration.unregister()`.
After the user visits a page that has `serviceWorkerRegistration.unregister()`,
the service worker will be uninstalled. Note that depending on how `/service-worker.js` is served,
it may take up to 24 hours for the cache to be invalidated.

### Offline-First Considerations

1. Service workers [require HTTPS][247],
although to facilitate local testing, that policy
[does not apply to `localhost`][248].
If your production web server does not support HTTPS, then the service worker
registration will fail, but the rest of your web app will remain functional.

1. Service workers are [not currently supported][249]
in all web browsers. Service worker registration [won't be attempted][250]
on browsers that lack support.

1. The service worker is only enabled in the [production environment][251],
e.g. the output of `npm run build`. It's recommended that you do not enable an
offline-first service worker in a development environment, as it can lead to
frustration when previously cached assets are used and do not include the latest
changes you've made locally.

1. If you *need* to test your offline-first service worker locally, build
the application (using `npm run build`) and run a simple http server from your
build directory. After running the build script, `create-react-app` will give
instructions for one way to test your production build locally and the [deployment instructions][252] have
instructions for using other methods. \*Be sure to always use an
incognito window to avoid complications with your browser cache.\*

1. If possible, configure your production environment to serve the generated
`service-worker.js` [with HTTP caching disabled][253].
If that's not possible—[GitHub Pages][254], for instance, does not
allow you to change the default 10 minute HTTP cache lifetime—then be aware
that if you visit your production site, and then revisit again before
`service-worker.js` has expired from your HTTP cache, you'll continue to get
the previously cached assets from the service worker. If you have an immediate
need to view your updated production deployment, performing a shift-refresh
will temporarily disable the service worker and retrieve all assets from the
network.

1. Users aren't always familiar with offline-first web apps. It can be useful to
[let the user know][255]
when the service worker has finished populating your caches (showing a "This web
app works offline!" message) and also let them know when the service worker has
fetched the latest updates that will be available the next time they load the
page (showing a "New content is available; please refresh." message). Showing
this messages is currently left as an exercise to the developer, but as a
starting point, you can make use of the logic included in [`src/registerServiceWorker.js`][256], which
demonstrates which service worker lifecycle events to listen for to detect each
scenario, and which as a default, just logs appropriate messages to the
JavaScript console.

1. By default, the generated service worker file will not intercept or cache any
cross-origin traffic, like HTTP [API requests][257],
images, or embeds loaded from a different domain. If you would like to use a
runtime caching strategy for those requests, you can [`eject`][258]
and then configure the
[`runtimeCaching`][259]
option in the `SWPrecacheWebpackPlugin` section of
[`webpack.config.prod.js`][260].

### Progressive Web App Metadata

The default configuration includes a web app manifest located at
[`public/manifest.json`][261], that you can customize with
details specific to your web application.

When a user adds a web app to their homescreen using Chrome or Firefox on
Android, the metadata in [`manifest.json`][262] determines what
icons, names, and branding colors to use when the web app is displayed.
[The Web App Manifest guide][263]
provides more context about what each field means, and how your customizations
will affect your users' experience.

## Analyzing the Bundle Size

[Source map explorer][264] analyzes
JavaScript bundles using the source maps. This helps you understand where code
bloat is coming from.

To add Source map explorer to a Create React App project, follow these steps:

```sh
npm install --save source-map-explorer
```

Alternatively you may use `yarn`:

```sh
yarn add source-map-explorer
```

Then in `package.json`, add the following line to `scripts`:

```diff
   "scripts": {
+    "analyze": "source-map-explorer build/static/js/main.*",
     "start": "react-scripts start",
     "build": "react-scripts build",
     "test": "react-scripts test --env=jsdom",
```

Then to analyze the bundle run the production build then run the analyze
script.

```
npm run build
npm run analyze
```

## Deployment

`npm run build` creates a `build` directory with a production build of your app. Set up your favourite HTTP server so that a visitor to your site is served `index.html`, and requests to static paths like `/static/js/main.<hash>.js` are served with the contents of the `/static/js/main.<hash>.js` file.

### Static Server

For environments using [Node][265], the easiest way to handle this would be to install [serve][266] and let it handle the rest:

```sh
npm install -g serve
serve -s build
```

The last command shown above will serve your static site on the port **5000**. Like many of [serve][267]’s internal settings, the port can be adjusted using the `-p` or `--port` flags.

Run this command to get a full list of the options available:

```sh
serve -h
```

### Other Solutions

You don’t necessarily need a static server in order to run a Create React App project in production. It works just as fine integrated into an existing dynamic one.

Here’s a programmatic example using [Node][268] and [Express][269]:

```javascript
const express = require('express');
const path = require('path');
const app = express();

app.use(express.static(path.join(__dirname, 'build')));

app.get('/', function (req, res) {
  res.sendFile(path.join(__dirname, 'build', 'index.html'));
});

app.listen(9000);
```

The choice of your server software isn’t important either. Since Create React App is completely platform-agnostic, there’s no need to explicitly use Node.

The `build` folder with static assets is the only output produced by Create React App.

However this is not quite enough if you use client-side routing. Read the next section if you want to support URLs like `/todos/42` in your single-page app.

### Serving Apps with Client-Side Routing

If you use routers that use the HTML5 [`pushState` history API][270] under the hood (for example, [React Router][271] with `browserHistory`), many static file servers will fail. For example, if you used React Router with a route for `/todos/42`, the development server will respond to `localhost:3000/todos/42` properly, but an Express serving a production build as above will not.

This is because when there is a fresh page load for a `/todos/42`, the server looks for the file `build/todos/42` and does not find it. The server needs to be configured to respond to a request to `/todos/42` by serving `index.html`. For example, we can amend our Express example above to serve `index.html` for any unknown paths:

```diff
 app.use(express.static(path.join(__dirname, 'build')));

-app.get('/', function (req, res) {
+app.get('/*', function (req, res) {
   res.sendFile(path.join(__dirname, 'build', 'index.html'));
 });
```

If you’re using [Apache HTTP Server][272], you need to create a `.htaccess` file in the `public` folder that looks like this:

```
    Options -MultiViews
    RewriteEngine On
    RewriteCond %{REQUEST_FILENAME} !-f
    RewriteRule ^ index.html [QSA,L]
```

It will get copied to the `build` folder when you run `npm run build`. 

If you’re using [Apache Tomcat][273], you need to follow [this Stack Overflow answer][274].

Now requests to `/todos/42` will be handled correctly both in development and in production.

On a production build, and in a browser that supports [service workers][275],
the service worker will automatically handle all navigation requests, like for
`/todos/42`, by serving the cached copy of your `index.html`. This
service worker navigation routing can be configured or disabled by
[`eject`ing][276] and then modifying the
[`navigateFallback`][277]
and [`navigateFallbackWhitelist`][278]
options of the `SWPreachePlugin` [configuration][279].

### Building for Relative Paths

By default, Create React App produces a build assuming your app is hosted at the server root.<br>
To override this, specify the `homepage` in your `package.json`, for example:

```js
  "homepage": "http://mywebsite.com/relativepath",
```

This will let Create React App correctly infer the root path to use in the generated HTML file.

**Note**: If you are using `react-router@^4`, you can root `<Link>`s using the `basename` prop on any `<Router>`.<br>
More information [here][280].<br>
<br>
For example:
```js
<BrowserRouter basename="/calendar"/>
<Link to="/today"/> // renders <a href="/calendar/today">
```

#### Serving the Same Build from Different Paths

> Note: this feature is available with `react-scripts@0.9.0` and higher.

If you are not using the HTML5 `pushState` history API or not using client-side routing at all, it is unnecessary to specify the URL from which your app will be served. Instead, you can put this in your `package.json`:

```js
  "homepage": ".",
```

This will make sure that all the asset paths are relative to `index.html`. You will then be able to move your app from `http://mywebsite.com` to `http://mywebsite.com/relativepath` or even `http://mywebsite.com/relative/path` without having to rebuild it.

### [Azure][281]

See [this][282] blog post on how to deploy your React app to Microsoft Azure.

### [Firebase][283]

Install the Firebase CLI if you haven’t already by running `npm install -g firebase-tools`. Sign up for a [Firebase account][284] and create a new project. Run `firebase login` and login with your previous created Firebase account.

Then run the `firebase init` command from your project’s root. You need to choose the **Hosting: Configure and deploy Firebase Hosting sites** and choose the Firebase project you created in the previous step. You will need to agree with `database.rules.json` being created, choose `build` as the public directory, and also agree to **Configure as a single-page app** by replying with `y`.

```sh
    === Project Setup

    First, let's associate this project directory with a Firebase project.
    You can create multiple project aliases by running firebase use --add,
    but for now we'll just set up a default project.

    ? What Firebase project do you want to associate as default? Example app (example-app-fd690)

    === Database Setup

    Firebase Realtime Database Rules allow you to define how your data should be
    structured and when your data can be read from and written to.

    ? What file should be used for Database Rules? database.rules.json
    ✔  Database Rules for example-app-fd690 have been downloaded to database.rules.json.
    Future modifications to database.rules.json will update Database Rules when you run
    firebase deploy.

    === Hosting Setup

    Your public directory is the folder (relative to your project directory) that
    will contain Hosting assets to uploaded with firebase deploy. If you
    have a build process for your assets, use your build's output directory.

    ? What do you want to use as your public directory? build
    ? Configure as a single-page app (rewrite all urls to /index.html)? Yes
    ✔  Wrote build/index.html

    i  Writing configuration info to firebase.json...
    i  Writing project information to .firebaserc...

    ✔  Firebase initialization complete!
```

Now, after you create a production build with `npm run build`, you can deploy it by running `firebase deploy`.

```sh
    === Deploying to 'example-app-fd690'...

    i  deploying database, hosting
    ✔  database: rules ready to deploy.
    i  hosting: preparing build directory for upload...
    Uploading: [==============================          ] 75%✔  hosting: build folder uploaded successfully
    ✔  hosting: 8 files uploaded successfully
    i  starting release process (may take several minutes)...

    ✔  Deploy complete!

    Project Console: https://console.firebase.google.com/project/example-app-fd690/overview
    Hosting URL: https://example-app-fd690.firebaseapp.com
```

For more information see [Add Firebase to your JavaScript Project][285].

### [GitHub Pages][286]

> Note: this feature is available with `react-scripts@0.2.0` and higher.

#### Step 1: Add `homepage` to `package.json`

**The step below is important!**<br>
**If you skip it, your app will not deploy correctly.**

Open your `package.json` and add a `homepage` field:

```js
  "homepage": "https://myusername.github.io/my-app",
```

Create React App uses the `homepage` field to determine the root URL in the built HTML file.

#### Step 2: Install `gh-pages` and add `deploy` to `scripts` in `package.json`

Now, whenever you run `npm run build`, you will see a cheat sheet with instructions on how to deploy to GitHub Pages.

To publish it at [https://myusername.github.io/my-app][287], run:

```sh
npm install --save gh-pages
```

Alternatively you may use `yarn`:

```sh
yarn add gh-pages
```

Add the following scripts in your `package.json`:

```diff
  "scripts": {
+   "predeploy": "npm run build",
+   "deploy": "gh-pages -d build",
    "start": "react-scripts start",
    "build": "react-scripts build",
```

The `predeploy` script will run automatically before `deploy` is run.

#### Step 3: Deploy the site by running `npm run deploy`

Then run:

```sh
npm run deploy
```

#### Step 4: Ensure your project’s settings use `gh-pages`

Finally, make sure **GitHub Pages** option in your GitHub project settings is set to use the `gh-pages` branch:

<img src="http://i.imgur.com/HUjEr9l.png" width="500" alt="gh-pages branch setting">

#### Step 5: Optionally, configure the domain

You can configure a custom domain with GitHub Pages by adding a `CNAME` file to the `public/` folder.

#### Notes on client-side routing

GitHub Pages doesn’t support routers that use the HTML5 `pushState` history API under the hood (for example, React Router using `browserHistory`). This is because when there is a fresh page load for a url like `http://user.github.io/todomvc/todos/42`, where `/todos/42` is a frontend route, the GitHub Pages server returns 404 because it knows nothing of `/todos/42`. If you want to add a router to a project hosted on GitHub Pages, here are a couple of solutions:

* You could switch from using HTML5 history API to routing with hashes. If you use React Router, you can switch to `hashHistory` for this effect, but the URL will be longer and more verbose (for example, `http://user.github.io/todomvc/#/todos/42?_k=yknaj`). [Read more][288] about different history implementations in React Router.
* Alternatively, you can use a trick to teach GitHub Pages to handle 404 by redirecting to your `index.html` page with a special redirect parameter. You would need to add a `404.html` file with the redirection code to the `build` folder before deploying your project, and you’ll need to add code handling the redirect parameter to `index.html`. You can find a detailed explanation of this technique [in this guide][289].

### [Heroku][290]

Use the [Heroku Buildpack for Create React App][291].<br>
You can find instructions in [Deploying React with Zero Configuration][292].

#### Resolving Heroku Deployment Errors

Sometimes `npm run build` works locally but fails during deploy via Heroku. Following are the most common cases.

##### "Module not found: Error: Cannot resolve 'file' or 'directory'"

If you get something like this:

```
remote: Failed to create a production build. Reason:
remote: Module not found: Error: Cannot resolve 'file' or 'directory'
MyDirectory in /tmp/build_1234/src
```

It means you need to ensure that the lettercase of the file or directory you `import` matches the one you see on your filesystem or on GitHub.

This is important because Linux (the operating system used by Heroku) is case sensitive. So `MyDirectory` and `mydirectory` are two distinct directories and thus, even though the project builds locally, the difference in case breaks the `import` statements on Heroku remotes.

##### "Could not find a required file."

If you exclude or ignore necessary files from the package you will see a error similar this one:

```
remote: Could not find a required file.
remote:   Name: `index.html`
remote:   Searched in: /tmp/build_a2875fc163b209225122d68916f1d4df/public
remote:
remote: npm ERR! Linux 3.13.0-105-generic
remote: npm ERR! argv "/tmp/build_a2875fc163b209225122d68916f1d4df/.heroku/node/bin/node" "/tmp/build_a2875fc163b209225122d68916f1d4df/.heroku/node/bin/npm" "run" "build"
```

In this case, ensure that the file is there with the proper lettercase and that’s not ignored on your local `.gitignore` or `~/.gitignore_global`.

### [Netlify][293]

**To do a manual deploy to Netlify’s CDN:**

```sh
npm install netlify-cli
netlify deploy
```

Choose `build` as the path to deploy.

**To setup continuous delivery:**

With this setup Netlify will build and deploy when you push to git or open a pull request:

1. [Start a new netlify project][294]
2. Pick your Git hosting service and select your repository
3. Click `Build your site`

**Support for client-side routing:**

To support `pushState`, make sure to create a `public/_redirects` file with the following rewrite rules:

```
/*  /index.html  200
```

When you build the project, Create React App will place the `public` folder contents into the build output.

### [Now][295]

Now offers a zero-configuration single-command deployment. You can use `now` to deploy your app for free.

1. Install the `now` command-line tool either via the recommended [desktop tool][296] or via node with `npm install -g now`.

2. Build your app by running `npm run build`.

3. Move into the build directory by running `cd build`.

4. Run `now --name your-project-name` from within the build directory. You will see a **now.sh** URL in your output like this:

	```
	> Ready! https://your-project-name-tpspyhtdtk.now.sh (copied to clipboard)
	```

	Paste that URL into your browser when the build is complete, and you will see your deployed app.

Details are available in [this article.][297]

### [S3][298] and [CloudFront][299]

See this [blog post][300] on how to deploy your React app to Amazon Web Services S3 and CloudFront.

### [Surge][301]

Install the Surge CLI if you haven’t already by running `npm install -g surge`. Run the `surge` command and log in you or create a new account.

When asked about the project path, make sure to specify the `build` folder, for example:

```sh
       project path: /path/to/project/build
```

Note that in order to support routers that use HTML5 `pushState` API, you may want to rename the `index.html` in your build folder to `200.html` before deploying to Surge. This [ensures that every URL falls back to that file][302].

## Advanced Configuration

You can adjust various development and production settings by setting environment variables in your shell or with [.env][303].

Variable | Development | Production | Usage
:--- | :---: | :---: | :---
BROWSER | :white\_check\_mark: | :x: | By default, Create React App will open the default system browser, favoring Chrome on macOS. Specify a [browser][304] to override this behavior, or set it to `none` to disable it completely. If you need to customize the way the browser is launched, you can specify a node script instead. Any arguments passed to `npm start` will also be passed to this script, and the url where your app is served will be the last argument. Your script's file name must have the `.js` extension.
HOST | :white\_check\_mark: | :x: | By default, the development web server binds to `localhost`. You may use this variable to specify a different host.
PORT | :white\_check\_mark: | :x: | By default, the development web server will attempt to listen on port 3000 or prompt you to attempt the next available port. You may use this variable to specify a different port.
HTTPS | :white\_check\_mark: | :x: | When set to `true`, Create React App will run the development server in `https` mode.
PUBLIC\_URL | :x: | :white\_check\_mark: | Create React App assumes your application is hosted at the serving web server's root or a subpath as specified in [`package.json` (`homepage`)][305]. Normally, Create React App ignores the hostname. You may use this variable to force assets to be referenced verbatim to the url you provide (hostname included). This may be particularly useful when using a CDN to host your application.
CI | :large\_orange\_diamond: | :white\_check\_mark: | When set to `true`, Create React App treats warnings as failures in the build. It also makes the test runner non-watching. Most CIs set this flag by default.
REACT\_EDITOR | :white\_check\_mark: | :x: | When an app crashes in development, you will see an error overlay with clickable stack trace. When you click on it, Create React App will try to determine the editor you are using based on currently running processes, and open the relevant source file. You can [send a pull request to detect your editor of choice][306]. Setting this environment variable overrides the automatic detection. If you do it, make sure your systems [PATH][307] environment variable points to your editor’s bin folder.
CHOKIDAR\_USEPOLLING | :white\_check\_mark: | :x: | When set to `true`, the watcher runs in polling mode, as necessary inside a VM. Use this option if `npm start` isn't detecting changes.
GENERATE\_SOURCEMAP | :x: | :white\_check\_mark: | When set to `false`, source maps are not generated for a production build. This solves OOM issues on some smaller machines.

## Troubleshooting

### `npm start` doesn’t detect changes

When you save a file while `npm start` is running, the browser should refresh with the updated code.<br>
If this doesn’t happen, try one of the following workarounds:

* If your project is in a Dropbox folder, try moving it out.
* If the watcher doesn’t see a file called `index.js` and you’re referencing it by the folder name, you [need to restart the watcher][308] due to a Webpack bug.
* Some editors like Vim and IntelliJ have a “safe write” feature that currently breaks the watcher. You will need to disable it. Follow the instructions in [“Adjusting Your Text Editor”][309].
* If your project path contains parentheses, try moving the project to a path without them. This is caused by a [Webpack watcher bug][310].
* On Linux and macOS, you might need to [tweak system settings][311] to allow more watchers.
* If the project runs inside a virtual machine such as (a Vagrant provisioned) VirtualBox, create an `.env` file in your project directory if it doesn’t exist, and add `CHOKIDAR_USEPOLLING=true` to it. This ensures that the next time you run `npm start`, the watcher uses the polling mode, as necessary inside a VM.

If none of these solutions help please leave a comment [in this thread][312].

### `npm test` hangs on macOS Sierra

If you run `npm test` and the console gets stuck after printing `react-scripts test --env=jsdom` to the console there might be a problem with your [Watchman][313] installation as described in [facebookincubator/create-react-app#713][314].

We recommend deleting `node_modules` in your project and running `npm install` (or `yarn` if you use it) first. If it doesn't help, you can try one of the numerous workarounds mentioned in these issues:

* [facebook/jest#1767][315]
* [facebook/watchman#358][316]
* [ember-cli/ember-cli#6259][317]

It is reported that installing Watchman 4.7.0 or newer fixes the issue. If you use [Homebrew][318], you can run these commands to update it:

```
watchman shutdown-server
brew update
brew reinstall watchman
```

You can find [other installation methods][319] on the Watchman documentation page.

If this still doesn’t help, try running `launchctl unload -F ~/Library/LaunchAgents/com.github.facebook.watchman.plist`.

There are also reports that *uninstalling* Watchman fixes the issue. So if nothing else helps, remove it from your system and try again.

### `npm run build` exits too early

It is reported that `npm run build` can fail on machines with limited memory and no swap space, which is common in cloud environments. Even with small projects this command can increase RAM usage in your system by hundreds of megabytes, so if you have less than 1 GB of available memory your build is likely to fail with the following message:

>  The build failed because the process exited too early. This probably means the system ran out of memory or someone called `kill -9` on the process.

If you are completely sure that you didn't terminate the process, consider [adding some swap space][320] to the machine you’re building on, or build the project locally.

### `npm run build` fails on Heroku

This may be a problem with case sensitive filenames.
Please refer to [this section][321].

### Moment.js locales are missing

If you use a [Moment.js][322], you might notice that only the English locale is available by default. This is because the locale files are large, and you probably only need a subset of [all the locales provided by Moment.js][323].

To add a specific Moment.js locale to your bundle, you need to import it explicitly.<br>
For example:

```js
import moment from 'moment';
import 'moment/locale/fr';
```

If import multiple locales this way, you can later switch between them by calling `moment.locale()` with the locale name:

```js
import moment from 'moment';
import 'moment/locale/fr';
import 'moment/locale/es';

// ...

moment.locale('fr');
```

This will only work for locales that have been explicitly imported before.

### `npm run build` fails to minify

You may occasionally find a package you depend on needs compiled or ships code for a non-browser environment.<br>
This is considered poor practice in the ecosystem and does not have an escape hatch in Create React App.<br>
<br>
To resolve this:
1. Open an issue on the dependency's issue tracker and ask that the package be published pre-compiled (retaining ES6 Modules).
2. Fork the package and publish a corrected version yourself.
3. If the dependency is small enough, copy it to your `src/` folder and treat it as application code.

## Something Missing?

If you have ideas for more “How To” recipes that should be on this page, [let us know][324] or [contribute some!][325]

[1]:	https://github.com/facebookincubator/create-react-app
[2]:	https://github.com/facebookincubator/create-react-app/blob/master/packages/react-scripts/template/README.md
[3]:	#updating-to-new-releases
[4]:	#sending-feedback
[5]:	#folder-structure
[6]:	#available-scripts
[7]:	#npm-start
[8]:	#npm-test
[9]:	#npm-run-build
[10]:	#npm-run-eject
[11]:	#supported-language-features-and-polyfills
[12]:	#syntax-highlighting-in-the-editor
[13]:	#displaying-lint-output-in-the-editor
[14]:	#debugging-in-the-editor
[15]:	#formatting-code-automatically
[16]:	#changing-the-page-title
[17]:	#installing-a-dependency
[18]:	#importing-a-component
[19]:	#code-splitting
[20]:	#adding-a-stylesheet
[21]:	#post-processing-css
[22]:	#adding-a-css-preprocessor-sass-less-etc
[23]:	#adding-images-fonts-and-files
[24]:	#using-the-public-folder
[25]:	#changing-the-html
[26]:	#adding-assets-outside-of-the-module-system
[27]:	#when-to-use-the-public-folder
[28]:	#using-global-variables
[29]:	#adding-bootstrap
[30]:	#using-a-custom-theme
[31]:	#adding-flow
[32]:	#adding-custom-environment-variables
[33]:	#referencing-environment-variables-in-the-html
[34]:	#adding-temporary-environment-variables-in-your-shell
[35]:	#adding-development-environment-variables-in-env
[36]:	#can-i-use-decorators
[37]:	#integrating-with-an-api-backend
[38]:	#node
[39]:	#ruby-on-rails
[40]:	#proxying-api-requests-in-development
[41]:	#invalid-host-header-errors-after-configuring-proxy
[42]:	#configuring-the-proxy-manually
[43]:	#configuring-a-websocket-proxy
[44]:	#using-https-in-development
[45]:	#generating-dynamic-meta-tags-on-the-server
[46]:	#pre-rendering-into-static-html-files
[47]:	#injecting-data-from-the-server-into-the-page
[48]:	#running-tests
[49]:	#filename-conventions
[50]:	#command-line-interface
[51]:	#version-control-integration
[52]:	#writing-tests
[53]:	#testing-components
[54]:	#using-third-party-assertion-libraries
[55]:	#initializing-test-environment
[56]:	#focusing-and-excluding-tests
[57]:	#coverage-reporting
[58]:	#continuous-integration
[59]:	#disabling-jsdom
[60]:	#snapshot-testing
[61]:	#editor-integration
[62]:	#developing-components-in-isolation
[63]:	#getting-started-with-storybook
[64]:	#getting-started-with-styleguidist
[65]:	#making-a-progressive-web-app
[66]:	#opting-out-of-caching
[67]:	#offline-first-considerations
[68]:	#progressive-web-app-metadata
[69]:	#analyzing-the-bundle-size
[70]:	#deployment
[71]:	#static-server
[72]:	#other-solutions
[73]:	#serving-apps-with-client-side-routing
[74]:	#building-for-relative-paths
[75]:	#azure
[76]:	#firebase
[77]:	#github-pages
[78]:	#heroku
[79]:	#netlify
[80]:	#now
[81]:	#s3-and-cloudfront
[82]:	#surge
[83]:	#advanced-configuration
[84]:	#troubleshooting
[85]:	#npm-start-doesnt-detect-changes
[86]:	#npm-test-hangs-on-macos-sierra
[87]:	#npm-run-build-exits-too-early
[88]:	#npm-run-build-fails-on-heroku
[89]:	#npm-run-build-fails-to-minify
[90]:	#momentjs-locales-are-missing
[91]:	#something-missing
[92]:	https://github.com/facebookincubator/create-react-app/blob/master/CHANGELOG.md
[93]:	https://github.com/facebookincubator/create-react-app/blob/master/CHANGELOG.md
[94]:	https://github.com/facebookincubator/create-react-app/issues
[95]:	http://localhost:3000
[96]:	#running-tests
[97]:	#deployment
[98]:	https://github.com/lukehoban/es6features
[99]:	https://github.com/rwaldron/exponentiation-operator
[100]:	https://github.com/tc39/ecmascript-asyncawait
[101]:	https://github.com/sebmarkbage/ecmascript-rest-spread
[102]:	https://github.com/tc39/proposal-dynamic-import
[103]:	https://github.com/tc39/proposal-class-public-fields
[104]:	https://facebook.github.io/react/docs/introducing-jsx.html
[105]:	https://flowtype.org/
[106]:	https://babeljs.io/docs/plugins/#presets-stage-x-experimental-presets-
[107]:	https://medium.com/@cpojer/effective-javascript-codemods-5a6686bb46fb
[108]:	https://en.wikipedia.org/wiki/Polyfill
[109]:	https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Global_Objects/Object/assign
[110]:	https://github.com/sindresorhus/object-assign
[111]:	https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise
[112]:	https://github.com/then/promise
[113]:	https://developer.mozilla.org/en/docs/Web/API/Fetch_API
[114]:	https://github.com/github/fetch
[115]:	https://babeljs.io/docs/editors
[116]:	https://github.com/jlongster/prettier
[117]:	https://code.visualstudio.com
[118]:	https://www.jetbrains.com/webstorm/
[119]:	https://code.visualstudio.com
[120]:	https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-chrome
[121]:	#advanced-configuration
[122]:	https://www.jetbrains.com/webstorm/
[123]:	https://chrome.google.com/webstore/detail/jetbrains-ide-support/hmhgeddbohgjknpmjagkdomcpobmllji
[124]:	#advanced-configuration
[125]:	https://github.com/prettier/prettier
[126]:	https://prettier.github.io/prettier/
[127]:	https://medium.com/@okonetchnikov/make-linting-great-again-f3890e1ad6b8
[128]:	https://github.com/prettier/prettier#editor-integration
[129]:	https://github.com/prettier/prettier#editor-integration
[130]:	#adding-a-stylesheet
[131]:	https://developer.mozilla.org/en-US/docs/Web/API/Document/title
[132]:	https://github.com/nfl/react-helmet
[133]:	#generating-dynamic-meta-tags-on-the-server
[134]:	#pre-rendering-into-static-html-files
[135]:	http://exploringjs.com/es6/ch_modules.html
[136]:	http://stackoverflow.com/questions/36795819/react-native-es-6-when-should-i-use-curly-braces-for-import/36796281#36796281
[137]:	http://stackoverflow.com/questions/36795819/react-native-es-6-when-should-i-use-curly-braces-for-import/36796281#36796281
[138]:	http://exploringjs.com/es6/ch_modules.html
[139]:	https://leanpub.com/understandinges6/read#leanpub-auto-encapsulating-code-with-modules
[140]:	http://2ality.com/2017/01/import-operator.html#loading-code-on-demand
[141]:	https://github.com/tc39/proposal-dynamic-import
[142]:	https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise
[143]:	http://serverless-stack.com/chapters/code-splitting-in-create-react-app.html
[144]:	https://github.com/AnomalyInnovations/serverless-stack-demo-client/tree/code-splitting-in-create-react-app
[145]:	https://webpack.js.org/
[146]:	https://medium.com/seek-ui-engineering/block-element-modifying-your-javascript-components-d7f99fcab52b
[147]:	https://github.com/postcss/autoprefixer
[148]:	https://github.com/postcss/autoprefixer#disabling
[149]:	https://facebook.github.io/react/docs/composition-vs-inheritance.html
[150]:	https://developer.mozilla.org/en-US/docs/Web/HTTP/Basics_of_HTTP/Data_URIs
[151]:	#changing-the-page-title
[152]:	#adding-a-stylesheet
[153]:	#adding-images-fonts-and-files
[154]:	#adding-a-stylesheet
[155]:	#adding-images-fonts-and-files
[156]:	https://developer.mozilla.org/en-US/docs/Web/Manifest
[157]:	http://github.hubspot.com/pace/docs/welcome/
[158]:	https://react-bootstrap.github.io
[159]:	https://gist.githubusercontent.com/gaearon/85d8c067f6af1e56277c82d19fd4da7b/raw/6158dd991b67284e9fc8d70b9d973efe87659d72/App.js
[160]:	https://medium.com/@tacomanator/customizing-create-react-app-aa9ffb88165
[161]:	https://medium.com/@preethikasireddy/why-use-static-types-in-javascript-part-1-8382da1e0adb
[162]:	http://flowtype.org/
[163]:	https://flowtype.org/docs/advanced-configuration.html
[164]:	https://nuclide.io/docs/languages/flow/
[165]:	https://flowtype.org/
[166]:	#injecting-data-from-the-server-into-the-page
[167]:	https://github.com/facebookincubator/create-react-app/issues/865#issuecomment-252199527
[168]:	#generating-dynamic-meta-tags-on-the-server
[169]:	https://github.com/motdotla/dotenv
[170]:	https://docs.travis-ci.com/user/environment-variables/
[171]:	https://devcenter.heroku.com/articles/config-vars
[172]:	https://medium.com/google-developers/exploring-es7-decorators-76ecb65fb841
[173]:	https://www.fullstackreact.com/articles/using-create-react-app-with-a-server/
[174]:	https://github.com/fullstackreact/food-lookup-demo
[175]:	https://www.fullstackreact.com/articles/how-to-get-create-react-app-to-work-with-your-rails-api/
[176]:	https://github.com/fullstackreact/food-lookup-demo-rails
[177]:	http://stackoverflow.com/questions/21854516/understanding-ajax-cors-and-security-considerations
[178]:	#configuring-the-proxy-manually
[179]:	http://enable-cors.org/server_expressjs.html
[180]:	#adding-custom-environment-variables
[181]:	https://medium.com/webpack/webpack-dev-server-middleware-security-issues-1489d950874a
[182]:	https://github.com/webpack/webpack-dev-server/issues/887
[183]:	https://github.com/facebookincubator/create-react-app/issues/2271
[184]:	https://github.com/chimurai/http-proxy-middleware#options
[185]:	https://github.com/nodejitsu/node-http-proxy#options
[186]:	https://socket.io/
[187]:	http://websocket.org/echo.html
[188]:	https://socket.io/docs/
[189]:	https://github.com/websockets/ws
[190]:	https://developer.mozilla.org/en-US/docs/Web/API/WebSocket
[191]:	#proxying-api-requests-in-development
[192]:	https://www.npmjs.com/package/react-snapshot
[193]:	https://medium.com/superhighfives/an-almost-static-stack-6df0a2791319
[194]:	https://medium.com/node-security/the-most-common-xss-vulnerability-in-react-js-applications-2bdffbcc1fa0
[195]:	https://github.com/facebookincubator/create-react-app/blob/master/CHANGELOG.md#migrating-from-023-to-030
[196]:	https://facebook.github.io/jest/
[197]:	https://facebook.github.io/jest/blog/2016/09/01/jest-15.html
[198]:	https://github.com/tmpvar/jsdom
[199]:	#continuous-integration
[200]:	http://facebook.github.io/jest/docs/expect.html
[201]:	http://facebook.github.io/jest/docs/expect.html#tohavebeencalled
[202]:	http://airbnb.io/enzyme/docs/api/shallow.html
[203]:	http://airbnb.io/enzyme/
[204]:	http://airbnb.io/enzyme/docs/api/mount.html
[205]:	http://airbnb.io/enzyme/
[206]:	http://facebook.github.io/jest/docs/expect.html
[207]:	http://chaijs.com/
[208]:	https://github.com/blainekasten/enzyme-matchers
[209]:	#initializing-test-environment
[210]:	https://github.com/facebook/jest/issues/new
[211]:	https://github.com/facebook/jest/pull/1566
[212]:	http://chaijs.com/
[213]:	http://sinonjs.org/
[214]:	https://docs.travis-ci.com/user/getting-started/
[215]:	https://travis-ci.org/profile
[216]:	https://docs.travis-ci.com/user/customizing-the-build/
[217]:	https://medium.com/@knowbody/circleci-and-zeits-now-sh-c9b7eebcd3c1
[218]:	https://github.com/facebookincubator/create-react-app/issues/new
[219]:	https://github.com/tmpvar/jsdom
[220]:	https://facebook.github.io/react/docs/top-level-api.html#reactdom.render
[221]:	https://facebook.github.io/react/docs/test-utils.html#renderintodocument
[222]:	https://github.com/facebook/react/blob/34761cf9a252964abfaab6faf74d473ad95d1f21/src/test/ReactTestUtils.js#L83-L91
[223]:	http://airbnb.io/enzyme/docs/api/mount.html
[224]:	http://airbnb.io/enzyme/index.html
[225]:	https://facebook.github.io/react/docs/test-utils.html#shallow-rendering
[226]:	http://airbnb.io/enzyme/docs/api/shallow.html
[227]:	http://airbnb.io/enzyme/index.html
[228]:	http://facebook.github.io/jest/blog/2016/07/27/jest-14.html
[229]:	http://facebook.github.io/jest/blog/2016/07/27/jest-14.html
[230]:	https://code.visualstudio.com
[231]:	https://github.com/orta/vscode-jest
[232]:	https://storybook.js.org
[233]:	https://github.com/storybooks/storybook
[234]:	https://react-styleguidist.js.org/
[235]:	https://github.com/styleguidist/react-styleguidist
[236]:	https://egghead.io/lessons/react-getting-started-with-react-storybook
[237]:	https://github.com/storybooks/storybook
[238]:	https://storybook.js.org/basics/introduction/
[239]:	https://github.com/storybooks/storybook/tree/master/addons/storyshots
[240]:	https://github.com/styleguidist/react-styleguidist
[241]:	https://react-styleguidist.js.org/docs/getting-started.html
[242]:	https://developers.google.com/web/progressive-web-apps/
[243]:	https://github.com/goldhand/sw-precache-webpack-plugin
[244]:	https://developers.google.com/web/fundamentals/instant-and-offline/offline-cookbook/#cache-falling-back-to-network
[245]:	src/index.js
[246]:	src/index.js
[247]:	https://developers.google.com/web/fundamentals/getting-started/primers/service-workers#you_need_https
[248]:	http://stackoverflow.com/questions/34160509/options-for-testing-service-workers-via-http/34161385#34161385
[249]:	https://jakearchibald.github.io/isserviceworkerready/
[250]:	src/registerServiceWorker.js
[251]:	#deployment
[252]:	#deployment
[253]:	http://stackoverflow.com/questions/38843970/service-worker-javascript-update-frequency-every-24-hours
[254]:	#github-pages
[255]:	https://developers.google.com/web/fundamentals/instant-and-offline/offline-ux#inform_the_user_when_the_app_is_ready_for_offline_consumption
[256]:	src/registerServiceWorker.js
[257]:	#integrating-with-an-api-backend
[258]:	#npm-run-eject
[259]:	https://github.com/GoogleChrome/sw-precache#runtimecaching-arrayobject
[260]:	../config/webpack.config.prod.js
[261]:	public/manifest.json
[262]:	public/manifest.json
[263]:	https://developers.google.com/web/fundamentals/engage-and-retain/web-app-manifest/
[264]:	https://www.npmjs.com/package/source-map-explorer
[265]:	https://nodejs.org/
[266]:	https://github.com/zeit/serve
[267]:	https://github.com/zeit/serve
[268]:	https://nodejs.org/
[269]:	http://expressjs.com/
[270]:	https://developer.mozilla.org/en-US/docs/Web/API/History_API#Adding_and_modifying_history_entries
[271]:	https://github.com/ReactTraining/react-router
[272]:	https://httpd.apache.org/
[273]:	http://tomcat.apache.org/
[274]:	https://stackoverflow.com/a/41249464/4878474
[275]:	https://developers.google.com/web/fundamentals/getting-started/primers/service-workers
[276]:	#npm-run-eject
[277]:	https://github.com/GoogleChrome/sw-precache#navigatefallback-string
[278]:	https://github.com/GoogleChrome/sw-precache#navigatefallbackwhitelist-arrayregexp
[279]:	../config/webpack.config.prod.js
[280]:	https://reacttraining.com/react-router/web/api/BrowserRouter/basename-string
[281]:	https://azure.microsoft.com/
[282]:	https://medium.com/@to_pe/deploying-create-react-app-on-microsoft-azure-c0f6686a4321
[283]:	https://firebase.google.com/
[284]:	https://console.firebase.google.com/
[285]:	https://firebase.google.com/docs/web/setup
[286]:	https://pages.github.com/
[287]:	https://myusername.github.io/my-app
[288]:	https://reacttraining.com/react-router/web/api/Router
[289]:	https://github.com/rafrex/spa-github-pages
[290]:	https://www.heroku.com/
[291]:	https://github.com/mars/create-react-app-buildpack
[292]:	https://blog.heroku.com/deploying-react-with-zero-configuration
[293]:	https://www.netlify.com/
[294]:	https://app.netlify.com/signup
[295]:	https://zeit.co/now
[296]:	https://zeit.co/download
[297]:	https://zeit.co/blog/unlimited-static
[298]:	https://aws.amazon.com/s3
[299]:	https://aws.amazon.com/cloudfront/
[300]:	https://medium.com/@omgwtfmarc/deploying-create-react-app-to-s3-or-cloudfront-48dae4ce0af
[301]:	https://surge.sh/
[302]:	https://surge.sh/help/adding-a-200-page-for-client-side-routing
[303]:	#adding-development-environment-variables-in-env
[304]:	https://github.com/sindresorhus/opn#app
[305]:	#building-for-relative-paths
[306]:	https://github.com/facebookincubator/create-react-app/issues/2636
[307]:	https://en.wikipedia.org/wiki/PATH_(variable)
[308]:	https://github.com/facebookincubator/create-react-app/issues/1164
[309]:	https://webpack.js.org/guides/development/#adjusting-your-text-editor
[310]:	https://github.com/webpack/watchpack/issues/42
[311]:	https://webpack.github.io/docs/troubleshooting.html#not-enough-watchers
[312]:	https://github.com/facebookincubator/create-react-app/issues/659
[313]:	https://facebook.github.io/watchman/
[314]:	https://github.com/facebookincubator/create-react-app/issues/713
[315]:	https://github.com/facebook/jest/issues/1767
[316]:	https://github.com/facebook/watchman/issues/358
[317]:	https://github.com/ember-cli/ember-cli/issues/6259
[318]:	http://brew.sh/
[319]:	https://facebook.github.io/watchman/docs/install.html#build-install
[320]:	https://www.digitalocean.com/community/tutorials/how-to-add-swap-on-ubuntu-14-04
[321]:	#resolving-heroku-deployment-errors
[322]:	https://momentjs.com/
[323]:	https://momentjs.com/#multiple-locale-support
[324]:	https://github.com/facebookincubator/create-react-app/issues
[325]:	https://github.com/facebookincubator/create-react-app/edit/master/packages/react-scripts/template/README.md

[image-1]:	http://facebook.github.io/jest/img/blog/15-watch.gif
[image-2]:	http://i.imgur.com/5bFhnTS.png
[image-3]:	https://cloud.githubusercontent.com/assets/49038/20795349/a032308a-b7c8-11e6-9b34-7eeac781003f.png
[image-4]:	http://i.imgur.com/7CIAWpB.gif