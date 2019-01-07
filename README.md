# Electron/Angular - quickstart

This is a blank project for Electron/Angular applications. It was generated with [Angular CLI](https://github.com/angular/angular-cli) version 1.6.3 and is using Electon v3.0.10 / Angular v7.1.0 and Angular CLI v7.0.6 at the moment.

## Features

### Customizable title bar
The main application window is set to frameless and there is a "titlebar" component in Angular that looks like Windows 10's default titlebar. If you don't want to use it, just set from the environment the frame of the application window to "true" and remove the component.

### Remembering of window width/height and position
Electron backend utilizes [electron-window-state](https://github.com/mawie81/electron-window-state#readme) for keeping the last position and dimensions of BrowserWindow.

## How to use

### Requirements

The only requirement is that you must have installed [Angular CLI](https://github.com/angular/angular-cli) globally.

```
npm install -g @angular/cli@latest
```

### Steps to create your application

First clone this repository (replace **YOUR-PROJECT-NAME** with the name of your project):

```
git clone https://github.com/D-LUSiON/electron-angular-quickstart YOUR-PROJECT-NAME
```

Then enter newly created directory and install dependancies:

```
cd YOUR-PROJECT-NAME
npm install
```

The dependancies of Angular and Electron are split into two. The dependancies of Angular are in **./package.json** and the dependancies of Electron are in **./electron/package.json** so you'll have to install these dependancies as well:

```
cd electron
npm install
```

*(This step will be automated in next releases)*

Now open your favourite editor and edit **./package.json** and **./electron/package.json**.

Change **"name"**, **"productName"** and **"description"** with something that describes what you plan to do. Now change **"author"** with your name and set the **"version"** of your application to "1.0.0" (you can read more about semantic versioning [here](https://semver.org/)). Of course you can change the **"license"** and **"keywords"** if you wish.

Save your changes and edit **./angular.json**

Find and replace all ***eaqs*** with abbreviation of the name of your application.

By default, Angular schematics uses "app" as component/directive prefix. If you want to change it, you can do it by editing value of **"prefix"** in **"schematics"**:

```
"schematics": {
    "@schematics/angular:component": {
        "prefix": "YOUR-APP-PREFIX",
        "styleext": "scss"
    },
    "@schematics/angular:directive": {
        "prefix": "YOUR-APP-PREFIX"
    }
}
```

Also don't forget to change the page title in **./src/index.html**!

With that everything's good to go and you can start developing your awesome application!

## Development server

Run `npm start` for a dev server. The Electron window will hot reload on any change.

## Build

Run `npm build` for interactive building and creating installer. It's tested under Win10 so I'll appreciate feedback for Linux and MacOS.



## License

This project is licensed under MIT license and you can do whatever you want with the code.
## Disclaimer

This project is still in early development and there might be unwanted bugs. If you see any just write an [issue](https://github.com/D-LUSiON/electron-angular-quickstart/issues) so I can fix it.
