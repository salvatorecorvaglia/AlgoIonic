# AlgoIonic

## Ionic SDK integration (Angular Framework) for Algorand SDK

[Ionic Framework](https://ionicframework.com) focuses on the frontend UX and UI interaction of an app — UI controls, interactions, gestures, animations. It’s easy to learn, and integrates with other libraries or Frameworks, such as [Angular](https://angular.io), [React](https://reactjs.org), or [Vue](https://vuejs.org). Alternatively, it can be used standalone without any frontend Framework using a simple [script](https://ionicframework.com/docs/intro/cdn) include.

### Requirements

- [Node and npm](https://nodejs.org)
- [Angular](https://angular.io)
- [React](https://reactjs.org)
- [Vue](https://vuejs.org)
- [AlgoSDK](https://github.com/algorand/js-algorand-sdk)
- [Ionic Framework](https://ionicframework.com)

### 1. Install Node and npm environment

To get started with Ionic Framework, the only requirement is Node and npm environment. Almost all tooling for modern JavaScript projects is based in [Node.js](https://nodejs.org/) (Node is bundled with npm, the package manager for JavaScript).

To verify the installation, open a new terminal window and run:

```
~$ node --version
14.17.0
~$ npm --version
6.14.13
```

### 2. Installing Ionic

Install the Ionic CLI with npm:

```
~$ npm install -g @ionic/cli
```

``
The -g option means install globally.
``

To verify the installation, open a terminal window and run:

```
~$ ionic -v
6.16.3
```

### 3. Create Ionic app

To create an Ionic App there are pre-made app templates, or a blank one to start fresh. The three most common starters are the ``blank starter``, ``tabs starter``, and ``sidemenu starter``. Get started with the ionic start command using ``tabs starter``:

```
~$ ionic start AlgoIonic tabs
```

When creating the project you will have to choose the Framework to interact with. In this case [Angular](https://angular.io/) is chosen.

```
Please select the JavaScript Framework to use for your new app. To bypass this
prompt next time, supply a value for the --type option.

✔ Framework: (Use arrow keys)
❯ Angular | https://angular.io
  React   | https://reactjs.org
  Vue     | https://vuejs.org

✔ Framework: Angular
✔ Preparing directory ./AlgoIonic in 3.93ms
✔ Downloading and extracting tabs starter in 393.38ms
```

The second step is to decide whether to integrate [Capacitor](https://capacitorjs.com), a cross-platform app runtime that makes it easy to build web apps that run natively on iOS, Android, Electron and the Web.

```
✔ Integrate your new app with Capacitor to target native iOS and Android? Yes
> ionic integrations enable capacitor --quiet -- AlgoIonic io.ionic.starter
> npm i --save -E @capacitor/core@latest
npm notice created a lockfile as package-lock.json. You should commit this file.
npm WARN The package @angular/compiler is included as both a dev and production dependency.

+ @capacitor/core@3.1.1
added 2 packages from 2 contributors and audited 2 packages in 2.449s
found 0 vulnerabilities
```

### 4. Start AlgoIonic

The majority of Ionic app development can be spent right in the browser using the ``ionic serve`` command:

```
~$ cd AlgoIonic
~/AlgoIonic$ ionic serve
> ng run app:serve --host=localhost --port=8100
[ng] ✔ Compiled successfully.

[INFO] Development server running!

       Local: http://localhost:8100

       Use Ctrl+C to quit this process

[INFO] Browser window opened to http://localhost:8100!

[ng] ✔ Browser application bundle generation complete.
[ng] 64 unchanged chunks
[ng] Build at: 2021-07-21T10:49:48.146Z - Hash: 4fee104eefbec3e20808 - Time: 1025ms
[ng] ✔ Compiled successfully.
```

### 5. Integrate AlgoSDK

Now it can be integrated [AlgoSDK](https://github.com/algorand/js-algorand-sdk), the official JavaScript library for communicating with the Algorand network, into the Ionic project:

```
~/AlgoIonic$ npm install algosdk
```

Now AlgoSDK is integrated in package.json installed in the dependencies:

```
"dependencies": {
    "@angular/common": "~12.1.1",
    "@angular/compiler": "~12.1.1",
    "@angular/core": "~12.1.1",
    "@angular/forms": "~12.1.1",
    "@angular/platform-browser": "~12.1.1",
    "@angular/platform-browser-dynamic": "~12.1.1",
    "@angular/router": "~12.1.1",
    "@capacitor/app": "1.0.2",
    "@capacitor/core": "3.1.1",
    "@capacitor/haptics": "1.0.2",
    "@capacitor/keyboard": "1.0.2",
    "@capacitor/status-bar": "1.0.2",
    "@ionic/angular": "^5.5.2",
    "algosdk": "^1.10.0",
    "rxjs": "~6.6.0",
    "tslib": "^2.2.0",
    "zone.js": "~0.11.4"
  },
```

From this moment it is possible to interact with the Algorand network and start developing any project with the Ionic Framework.
