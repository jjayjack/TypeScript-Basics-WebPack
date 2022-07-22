# TypeScript-Basics-WebPack

## About

You get the best of both worlds! Disadvantage of using ES Modules is that you are using loads of get requests which takes time to run request and send it to the page.
[WebPack](https://webpack.js.org/) is a tool that using [Node JS](https://nodejs.org/en/) bundles files together. This tools allows larger packages of code to be bundled together with less imports required and let's us run a smoother application without a heavy coded application. WebPack allows us to plug in functionality to an application. It allows us to transform our code.

## To Begin

Install dependencies for development:
ts-loader
typescript
webpack
webpack-cli
webpack-dev-server

## Working with webpack.config.js

Working with the webpack configure JavaScript file sets up where Webpack must run and get correct paths to files.

To set up how WebPack reads **module rules**. First set is the `test` property that WebPack will perform on files. The `use` property is defined next to set the loader WebPack will use. Last the `exclude` property will be set to make sure node\*modules are not added to the WebPack compilation.

Next the **resolve key** will be set. This notifies WebPack what file extensions to add to inputs found. For this project TypeScript and JavaScript files should be the targets for which files we want Webpack to look for.

_Check that within `tsconfig`, sourceMap is set to true._

The `devtool` property should be set so that WebPack knows there should be source maps already.

Within the **package.json** file a new script must be set to run webpack. Then remove everything that has been rendered with the dist folder and run `npm run build` to create a WebPack compiled dist component.

### Updating Configs to run Server in Dev Mode

Start by updating **package.json** with script `"start":"webpack-dev-server"`

This change will allow the application to run your Server in development mode.

Next update **webpack.config.js** with adding output `publicPath: 'dist'`. Also add mode to `development`.
