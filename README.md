[![Build Status](https://travis-ci.org/thiren/angular-seed.svg?branch=master)](https://travis-ci.org/thiren/angular-seed)

# angular-seed
A project seed for new angular applications


## Getting Started

To get you started you can simply clone the angular-seed repository and install the dependencies:

### Prerequisites

You need git to clone the angular-seed repository. You can get git from [http://git-scm.com/](http://git-scm.com/).

We also use a number of node.js tools to initialize and test angular-seed. You must have node.js and its package manager (npm) installed. You can get them from [http://nodejs.org/](http://nodejs.org/).

### Clone angular-seed

Clone the angular-seed repository using [git][git]:

```
git clone https://github.com/thiren/angular-seed.git
cd angular-seed
```

If you just want to start a new project without the angular-seed commit history then you can do:

```bash
git clone --depth=1 -b <branch_name> https://github.com/thiren/angular-seed.git <your-project-name>
```

The `depth=1` tells git to only pull down one commit worth of historical data.

### Install Dependencies

We have two kinds of dependencies in this project: tools and client-side framework code. The tools help us manage and test the application.

* We get the tools we depend upon via `npm`, the [node package manager][npm]
* We get the client-side framework code via `bower`, a [client-side code package manager][bower]

We have preconfigured `npm` to automatically run `bower` so we can simply do:

```
npm install
```

Behind the scenes this will also call `bower install`. You should find that you have two new folders in your project.

* `node_modules` - contains the npm packages for the tools we need
* `bower_components` - contains the client-side framework files

In order to build the application you will need to install the [Gulp][gulp] build system globally.

```
npm install -g gulp
```

### Run the Application

We have preconfigured the project with a build process and a simple development web server. This build process is written using the [Gulp][gulp] build system. The simplest way to build the application and start this server is:

```
gulp watch --env=dev
```

The `--env=dev` tells the build process that we want to build the application for the `dev` environment. The build process can be executed using four different environments: `dev`, `qa`, `localqa` or `production`. The build process will differ depending on which environment is specified when running the build. 

You should find that you have one new folder in your project.

* `build` - contains the built angular application and all static website resources

Now browse to the app at `http://localhost:9000`.

## Directory Layout

```
src/
  app/
    header/
      header.controller.js
      header.tpl.html
    app.module.js
    main.tpl.html
  configs/
    constants.json
  fonts/
  images/
  styles/
    main.less
  favicon.ico
  index.html
tests/
  unit/
    header/
      header.controller.spec.js
karma.config.js
build.config.js
gulpfile.js
```

## Testing

### Running Unit Tests
The angular-seed app comes preconfigured with unit tests. These are written using a combination of the [Mocha][mocha] testing framework, the [Chai][chai] assertion library and [Sinon][sinon] which allows us to write standalone test spies, stubs and mocks. We run the unit tests using the [Karma Test Runner][karma]. We provide a Karma configuration file to run them.

* The configuration is found in the `karma.conf.js` file
* The unit tests are found next to the code they are testing or in the `tests/unit` directory and are named as `<file_name>.spec.js`

The easiest way to run the unit tests is to use the supplied npm script:

```
npm test
```

This script will start the Karma test runner to execute the unit tests.

## Continuous Integration

### Travis CI

[Travis CI][travis] is a continuous integration service, which can monitor GitHub for new commits to your repository and execute scripts such as building the app or running tests. The angular-seed project contains a Travis configuration file, `.travis.yml`, which will cause Travis to run your tests when you push to GitHub.

You will need to enable the integration between Travis and GitHub. See the Travis website for more instruction on how to do this.

## Resources

For more information on AngularJS please check out [http://angularjs.org/](http://angularjs.org/)

[git]: http://git-scm.com/
[gulp]: http://gulpjs.com/
[bower]: http://bower.io
[npm]: https://www.npmjs.org/
[node]: http://nodejs.org
[protractor]: https://github.com/angular/protractor
[mocha]: https://mochajs.org/
[chai]: http://chaijs.com/
[sinon]: http://sinonjs.org/
[karma]: http://karma-runner.github.io
[travis]: https://travis-ci.org/
