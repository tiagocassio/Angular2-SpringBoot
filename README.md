# Angular2-SpringBoot
A quick starter project for angular 2 &amp; Spring Boot for Java developers.

Global install
- Install node.js
- npm install typescript -g (installs the typescript compiler, now available as command `tsc`)
- npm install gulp -g

In frontend folder
- npm install (downloads libraries)
- gulp setup-typings 
- gulp build (builds distro in the `dist`  folder)

Start up your Spring Boot application and navigate to
http://localhost:8080/app/root. You should see a `Click Me` button.

The Spring Boot application is connected to the `dist` folder thanks to the configuration in the WebMvcConfiguration class. 
In your browser dev tools you should see a directory app-src that contains the typescript files, ready for debugging.

Create a new project in Webstorm 11 (pre-release) with the frontend folder as root (not the main folder). 

Go to `File->Settings` and configure the Typescript Compiler so that it uses the tsconfig.json file, enable the typescript compiler and track changes. Mark your `dist` folder as an excluded directory.

You can right click your gulpfile.js and select `Show gulp tasks`. Run the `watch-resources` gulp task, this will track changes in html files and copy them to the `dist` folder. You can always do a clean build by running the `build` or `build-watch-resources` task.

Now you are ready to create Angular 2 applications and use your Spring Boot application to offer backend services at the same time.

For Java developers not familiar with javascript & typescript development, a more detailed introduction can be found at
[Angular2-Intro](https://github.com/Krustie101/Angular2-Intro).

