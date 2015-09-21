
<html lang="en" class="is-copy-enabled">
  <head>
    <meta charset='utf-8'>
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta http-equiv="Content-Language" content="en">
    <title>JavaScript SDK Project Setup</title>
  </head>

  <body>
  
<h2><a id="user-content-authors" class="anchor" href="#authors" aria-hidden="true"><span class="octicon octicon-link"></span></a>Authors</h2>

<p>Adarsh Kumar (<a href="mailto:adarsh.kumar@elliemae.com">adarsh.kumar@elliemae.com</a>)</p>

<h2><a id="user-content-download" class="anchor" href="#download" aria-hidden="true"><span class="octicon octicon-link"></span></a>Download</h2>

<p>You clone the project with Git by running:</p>

<pre><code>coming soon</code></pre>

# Step by step JavaScript SDK Project Setup on local computer

To be able to run and debug JavaScript SDK (Controls) on your local machine, Webstorm or Visual Studio IDE should be install and have TFS permission to get code on your local machine.

#Important Framework Files 

- Package.json: Package.json file have all the dev dependancies and required plugins names along with version fields.
- Gulp.js -  Gulp is the main build and deploy process file which help to run other plugins e.g. watch.
- Webpack.config.js  - To create bundles (JS,HTML,CSS,TAG etc) which will use to implement simple/complex controls on different project.
- Karma.conf.js - Karma is test runner framework to run jasmine written unit test cases and code coverage reports using isparta. We are using jasmine to write the unit test cases.
- Phantomcss.conf.js - Phantomcss helps to test functional/UI test cases. It internally use phantomJS, ResembleJS and casperjs to capture screenshot and compare it.
- CasperJS.bat - Configure phantomJS and slimmerJS(If required)
- Protractor.conf.js - To test complex and angular controls.
- Web.config - Configuratin to setup NodeJS on IIS
- app.js - Main NodeJS file to run server and presentation layer. 
- config.js - It's under gulpconfig folder. Project level configuration. Please use this file to put hardcode url and path.

Note: Please feel free to add/update more plugins if it helps to improve build process.
 
Please follow the below steps to setup on your local machine.

#Step 1: Download and install Node.js
 - Please use this link to install <a href="https://nodejs.org/">NodeJS</a> on your local machine. We need node to use npm to get all the dependent plugins e.g. Gulp, Karma etc.
 - If you are going to use the command line mode, make sure the following paths are added to the PATH variable:<br/>
    1. The path to the parent folder of the Node.js executable file.
    2. The path to the npm folder.This enables you to launch the npm from any folder.
    <img src="https://github.com/adars99/Controls_Setup/blob/master/images/Capture1.PNG"><br/>	
	
	
#Step 2: Install and setup TFS on Webstorm
 - Install and enable TFS on Webstorm IDE.
   1. Open Webstorm Idea IDE, go to File->Settings. Search "Plugins" on the left top search bar.
   2. Click on Install JetBrains Plugin button. 
   <img src="https://github.com/adars99/Controls_Setup/blob/master/images/Capture2.PNG"><br />
   3. Search TFS on Browse JetBrains Plugins window and click on install TFS Plugin button.
   <img src="https://github.com/adars99/Controls_Setup/blob/master/images/Capture3.PNG"><br />
   4. Connect to TFS from Webstorm IDE, go to VCS-> checkout from version control->TFS.
    <img src="https://github.com/adars99/Controls_Setup/blob/master/images/Capture4.PNG"><br/>
   5. Enter workspace name e.g. controls and click on next button.
	<img src="https://github.com/adars99/Controls_Setup/blob/master/images/Capture5.PNG"><br/>
   6. Click on Add button and enter TFS server info along with credentail (if you are trying to access outside of network) and press OK button.
	<img src="https://github.com/adars99/Controls_Setup/blob/master/images/Capture6.PNG"><br/>
   7. Click next button and select the destination local path where you want to keep local code.
	
#Step 3: Development installation
 - Launch the embedded Terminal by hovering your mouse pointer over in the lower left corner of Webstorm IDE and choosing Terminal from the menu.
 Or Open the command prompt as a administrator. 
<br/>
Note: NPM is required. cd to the root project directory and run. It will install all the required plugin mentioned in package.json.

 <br/>
<b>Installation - Use NPM</b>

```sh
$ npm install
```
#Step 4: Configuring Gulp on Webstorm  IDE.
 - We are using gulp to build the entire project. It calls different plugins e.g. webpack to build bundles, karma to run unit test etc. 
 1. Go to Run-> select Edit Configurations, on Run/Debug Configurations window, clik on "+" button and select Gulp.js.
	<img src="https://github.com/adars99/Controls_Setup/blob/master/images/Capture7.PNG"><br/>
 2. Enter the below configuration and click on OK button.	
	<img src="https://github.com/adars99/Controls_Setup/blob/master/images/Capture8.PNG"><br/>
	
Note: We can also use command prompt/visual studio task manager to run gulp. We prefer to use single IDE to do everything.
<br/>

<b>Run gulp on command prompt - Use NPM</b>
 	
```sh

$ gulp
```

#Step 5: Run JavaScript SDK(Controls) Project on your local

- Click on Run/Debug button, it will build the project and run unit test and finally open controls project on default browser.
 	
<img src="https://github.com/adars99/Controls_Setup/blob/master/images/Capture9.PNG"><br/>

### Tech Support

* Please make sure, you are not sitting on build folder e.g. main and release folders otherwise you will see "Operation Not permitted error"
* Please delete main and release folder if you are getting build errors during "copy" or "replace"
* Please use individual command to fix particular gulp plugin e.g. clean up use "gulp clean" in terminal or command prompt      
  </body>
</html>

