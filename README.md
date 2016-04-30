Checkout blog post for this here: http://www.tattoocoder.com/angular-2-getting-off-the-starting-line/

# ng2-startingline
Template based on https://github.com/angular/quickstart, added gulp build process.

### Prerequisites

* node.js >= 4.x
* gulp and gulp-cli
* typescript

```
npm install -g typescript gulp gulp-cli
```

### Start development

Install the npm packages described in the `package.json` and verify that it works:

```bash
npm install
npm start
```
You're ready to write your application.

Remember the npm scripts in `package.json`:

* `npm start` - runs the compiler and a server at the same time, both in "watch mode".
* `npm run tsc` - runs the TypeScript compiler once.
* `npm run tsc:w` - runs the TypeScript compiler in watch mode; the process keeps running, awaiting changes to TypeScript files and re-compiling when it sees them.
* `npm run lite` - runs the [lite-server](https://www.npmjs.com/package/lite-server), a light-weight, static file server, written and maintained by
[John Papa](https://github.com/johnpapa) and
[Christopher Martin](https://github.com/cgmartin)
with excellent support for Angular apps that use routing.
* `npm run typings` - runs the typings tool.
* `npm run postinstall` - called by *npm* automatically *after* it successfully completes package installation. This script installs the TypeScript definition files this app requires.

### Building Files

```
gulp clean
npm run build
```

This will build the application into the **/build** folder.  In order to run locally using the node.js server

```
cd build
node index.js
```

Uses gulp to transpile the Angular application, moves the _needed_ application files and dependencies to the `build` folder.

```
├─build
├── app
│   ├── app.component.js
│   ├── app.component.js.map
│   ├── main.js
│   └── main.js.map
├── index.html
├── index.js
├── node_modules
│   ├── angular2
│   │   ├── bundles
│   │   │   ├── angular2-polyfills.js
│   │   │   ├── angular2.dev.js
│   │   │   └── router.dev.js
│   │   └── es6
│   │       └── dev
│   │           └── src
│   │               └── testing
│   │                   └── shims_for_IE.js
│   ├── es6-shim
│   │   └── es6-shim.min.js
│   ├── rxjs
│   │   └── bundles
│   │       └── Rx.js
│   └── systemjs
│       └── dist
│           ├── system-polyfills.js
│           └── system.src.js
├── package.json
└── styles.css
```