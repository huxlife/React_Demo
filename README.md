# 部署 Github Pages 

## 1. 安装 gh-pages
    npm install gh-pages --save-dev
    
    如果失败，切换官方镜像源或者其他的
    npm config set registry https://registry.npmjs.org/
    npm config set registry https://registry.npm.taobao.org/
    
    如果安装失败，可以尝试使用 cnpm 安装
    npm install -g cnpm --registry=https://registry.npm.taobao.org
    cnpm install gh-pages --save-dev
    
## 2. 修改 package.json
    
    "homepage": "https://<username>.github.io/<repository-name>",
    "scripts": {
    "predeploy": "npm run build",
    "deploy": "gh-pages -d build"
    },
    
## 3. 部署
    npm run deploy  
    操作后，会生成一个分支 gh-pages，里面就是编译好的文件，然后就可以在浏览器中访问了。
    
    https://<username>.github.io/<repository-name>
    一般10分钟左右就可以访问了。
## 4. 常见问题
    1. 404
        1. 请检查是否在 package.json 中配置了 homepage
        2. 请检查是否在 package.json 中配置了正确的 scripts.deploy
        3. 请检查是否在 package.json 中配置了正确的 scripts.predeploy
    2. 显示了Readme.md
        1. 请检查是否在 package.json 中配置了正确的 scripts.deploy
        2. 请检查是否在 package.json 中配置了正确的 scripts.predeploy
        3. 请检查是否在 package.json 中配置了正确的 homepage
        4. 在 Settings Page 下面 检查是否配置了正确的 branch
     
# Getting Started with Create React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in your browser.

The page will reload when you make changes.\
You may also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can't go back!**

If you aren't satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you're on your own.

You don't have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn't feel obligated to use this feature. However we understand that this tool wouldn't be useful if you couldn't customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

### Code Splitting

This section has moved here: [https://facebook.github.io/create-react-app/docs/code-splitting](https://facebook.github.io/create-react-app/docs/code-splitting)

### Analyzing the Bundle Size

This section has moved here: [https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size](https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size)

### Making a Progressive Web App

This section has moved here: [https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app](https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app)

### Advanced Configuration

This section has moved here: [https://facebook.github.io/create-react-app/docs/advanced-configuration](https://facebook.github.io/create-react-app/docs/advanced-configuration)

### Deployment

This section has moved here: [https://facebook.github.io/create-react-app/docs/deployment](https://facebook.github.io/create-react-app/docs/deployment)

### `npm run build` fails to minify

This section has moved here: [https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify](https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify)
