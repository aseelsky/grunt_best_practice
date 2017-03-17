1) install node.js

2) Install grunt command interface globally (-g)
    $ npm install -g grunt-cli

Starting from here, this should be done every time you create a project:
3) $ npm init
    this creates package.json, this file contain all the dependencies/plugin so when the project downloaded from github and run the command $ npm install, they will be all downloaded

4) Install grunt and add it as a dependency to the package.json file by adding (--save-dev)
    (check package.json before the following)
    $ npm install grunt --save-dev
    (check package.json now)
    this creates node_modules folder with grunt in it.

5) Install the desire grunt plugin
    (check package.json before the following)
    $ npm install grunt-sass --save-dev
    (check package.json now)

6) Create Gruntfile.js file to config the grunt task

7) Configure grunt task using the plugin

    1st, Grunt wrapper:
   --------------------------------------------
   |  module.exports = function(grunt) {
   |
   |  }
   --------------------------------------------


    2nd, Load the plugin:
   --------------------------------------------
   |  module.exports = function(grunt) {
   |
   |    grunt.loadNpmTasks('grunt-sass');
   |
   |  }
   --------------------------------------------


    3rd, Configure the task using initConfig function:
   --------------------------------------------
   |  module.exports = function(grunt) {
   |    grunt.loadNpmTasks('grunt-sass');
   |
   |    grunt.initConfig({
   |      - - - -
   |      - - - -
   |      - - - -
   |    });
   |
   |  }
   --------------------------------------------


   4th, Register the task:
  --------------------------------------------
  |   module.exports = function(grunt) {
  |     grunt.loadNpmTasks('grunt-sass');
  |     grunt.initConfig({
  |       - - - -
  |       - - - -
  |       - - - -
  |     });
  |
  |     grunt.registerTask('default', ['sass']);
  |
  |  }
  --------------------------------------------

8) Run grunt command
    $ grunt

------------- Done -------------
Suggested plugins:
loard-grunt-tasks
grunt-contrib-watch
