<img src="https://cloud.githubusercontent.com/assets/668093/12567089/0ac42774-c372-11e5-97eb-00baf0fccc37.jpg" alt="OpenMRS"/>

# OpenMRS Open Web App Generator

[![Build Status](https://img.shields.io/travis/psbrandt/generator-openmrs-owa.svg?style=flat-square)](http://travis-ci.org/psbrandt/generator-openmrs-owa)
[![Downloads](https://img.shields.io/npm/dt/generator-openmrs-owa.svg?style=flat-square)](https://www.npmjs.com/package/generator-openmrs-owa)

> [Yeoman](http://yeoman.io) generator that scaffolds an [OpenMRS Open Web App](https://wiki.openmrs.org/display/docs/Open+Web+Apps+Module)

[![OpenMRS OWA Asciicast](screenshot.png)](https://asciinema.org/a/38974?autoplay=1)

## Features

The following features are currently supported:

  - [x] Scaffold basic OWA folder structure and files
  - [x] Production build with [Webpack](https://webpack.github.io/)
  - [x] Local deploy with Webpack
  - [x] Package management with [npm](http://npmjs.com/)
  - [x] Live reload, interaction sync and more with [Browsersync](https://www.browsersync.io/)

## Getting Started

 - Install dependencies: `npm install --global yo gulp bower`
 - Install the generator: `npm install --global generator-openmrs-owa`
 - Create directory for your app: `mkdir openmrs-owa-myapp && cd $_`
 - Run `yo openmrs-owa` to scaffold the Open Web App
 - Run `npm run build:prod` to build distributable zip file
 - Run `npm run build:deploy` to deploy directly to your local server
 - Run `npm run watch` for live reloading and more

## Extending

Install [npm](http://npmjs.com/) packages dependencies as follows:

````sh
npm install --save <package>
````

To use the installed package, import it as follows:

````js
//import and assign to variable
import variableName from 'package';
````

To contain package in vendor bundle, remember to add it to vendor entry point array, eg.:

````js
entry: {
  app : `${__dirname}/app/js/owa.js`,
  css: `${__dirname}/app/css/owa.css`,
  vendor : [
    'package',
    ...//other packages in vendor bundle
  ]
},
````

Any files that you add manually must be added in the `app` directory.

## Options

 - `--skip-welcome-message` Skips Yeoman's greeting before displaying options.
 - `--skip-install` Skips automatically running `npm install`.

## Environment Variables

The generator will read the following environment variables and use their values as the default when generating a new Open Web App:

- `OMRS_OWA_LOCAL_DIR`: The directory to use for local deployment

> e.g. `/Users/pascal/Downloads/openmrs-standalone-2.3.1/appdata/owa`

- `OMRS_OWA_GITHUB_ID`: Your GitHub username

> e.g. `psbrandt`

- `OMRS_OWA_BASE_URL`: The base URL of your local OpenMRS server

> e.g. `http://localhost:8082/openmrs-standalone`

## Contribute

See the [contributing docs](https://github.com/yeoman/yeoman/blob/master/contributing.md).

## Support

It's best to ask your questions on [OpenMRS talk](https://talk.openmrs.org/tags/c/software/javascript).

## License

[MPL-2.0](http://openmrs.org/license/)
