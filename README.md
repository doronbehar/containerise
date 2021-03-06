# <img src="https://raw.githubusercontent.com/kintesh/containerise/master/static/icons/icon.png" alt="Drawing" width="42" align="top"/> containerise [![Build Status](https://travis-ci.org/kintesh/containerise.svg?branch=master)](https://travis-ci.org/kintesh/containerise)

Firefox extension to automatically open websites in a container

|![](https://raw.githubusercontent.com/kintesh/containerise/master/static/screenshots/1.png)  |  ![](https://raw.githubusercontent.com/kintesh/containerise/master/static/screenshots/2.png)  |  ![](https://raw.githubusercontent.com/kintesh/containerise/master/static/screenshots/3.png)  |  ![](https://raw.githubusercontent.com/kintesh/containerise/master/static/screenshots/4.png)|
| --- | --- | --- | --- |
|Select your container and add a domain to always open all visits in the chosen container. | Add many domains as you wish. | Special `No Container` option to break out of a container. | Simple CSV based mapping of a domain to a container by name for easy backup and bulk editing. |


# Installation
Install the latest release for Firefox from [AMO](https://addons.mozilla.org/en-US/firefox/addon/containerise/)



# Usage

## Basic mapping
\
`amazon.co.uk, Shopping` will open all amazon.co.uk (not subdomains) links in Shopping container.

## Glob
`!*.amazon.co.uk, Shopping`  will be treated as `*.amazon.co.uk` glob pattern. (suitable to subdomains)

## Regex

`@.+\.amazon\.co\.uk$, Shopping` will be treat as `.+\.amazon\.co\.uk$` regex. (suitable to subdomains and complex paths)



# Development

## Available Scripts
In the project directory, you can run:

#### `yarn install`
Installs required dependencies. 

#### `yarn webpack`
Starts webpack with `--watch` option and outputs to `./build` directory.
 
#### `yarn build`
Builds the extension for production use.<br>

#### `yarn test`
Runs test specs using jest.
Use `test:watch` to watch for edits and re-run the tests.

#### `yarn lint`
Lint using eslint.

#### `yarn web-ext`
Runs web-ext process to debug the extension on Firefox. See [web-ext docs](https://github.com/mozilla/web-ext) <br/>
To live reload the extension, start this process in a new tab after starting `yarn webpack` process.
