# JS Boilerplate

This is a boilerplate to be used for JS-assignments in the course. The virtual machine (Ubuntu 32bit) will have the following default installed:
* node.js
* npm
* git 

Upon `npm install` the packages will be installed:
* bower
* browserify
* gulp
* sass
* jshint
* ...

## Install
Make sure you have the following installed on your system:
* Virtual Box [https://www.virtualbox.org/](https://www.virtualbox.org/)
* Vagrant [https://www.vagrantup.com/](https://www.vagrantup.com/)

Now, do:

1. Clone (`git clone https://github.com/1dv022/js-boilerplate.git`) this repro to the location you want the project to live. Note that git clone will create the directory `js-boilerplate` for you if you do not specify otherwise. 

2. Change directory to `cd js-boilerplate`. 

3. Start the virtual machine using `vagrant up` (Will take a couple of minutes)

4. SSH into the machine using  `vagrant ssh`

5. Change directory to `cd /vagrant`

6. Install all dependencies (incl. bower dependencies) `npm install` (Note: will take 5-10 minutes)

## Daily workflow
1. Start out by `vagrant up` your machine and ssh into it (`vagrant ssh`). Change directory to `cd /vagrant`.

2. Start watching for changes in the app-directory by `npm run gulp:watch`. Now you have a small webserver serving your application on the adress: `http://localhost:9090`, try it out in the browser of your choise.

3. Fire up the IDE of your choise (Webstorm, sublime etc.) and open the files in the `js-boilerplate`-folder or `js-boilerplate/app`-folder and start editing your application. If you make a change in an html-, css- or js-file the tasks for that file will run and the web page in your browser will autoreload.

4. When you are done simply `ctrl+c` to abort the watch, `exit` to  exit the ssh-session and do a `vagrant halt` to stop the machine or `vagrant suspend` to only suspend it.

## Running tasks
You find all prepered tasks in package.json under "scripts".

The most relevant are:
* `npm run gulp` Builds the system clean into the "dist"-folder
* `npm run gulo:build` Builds the system into the "dist"-folder
* `npm run gulp:watch` Watches for changes to .html, .scss and .js
