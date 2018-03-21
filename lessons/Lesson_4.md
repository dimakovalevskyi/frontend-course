# "Hello, world" app

## Steps:

 * prepare structure for project
 * download lib's files (angularjs, Bootstrap, materialize, any other)
 * commit now
 * install [Ruby](https://github.com/oneclick/rubyinstaller2/releases) and [sass](https://sass-scss.ru/install/) (otional)
 * install grunt and grunt-plugins:
   * grunt
   * grunt-contrib-sass
   * grunt-contrib-cssmin
   * grunt-contrib-uglify-es
   * grunt-contrib-watch
 * create empty `Gruntfile.js`
 * configurate every grunt plugin
 * what is `.map` file ?
 * write some css and js code to check how it works
 * final commit
 * configure gh-pages
 
## Project structure:
 
```
───application/
   │
   ├───css/
   │   └───src/
   │       ├───assets/
   │       └───main.scss
   ├───js/
   │   └───src/
   │       ├───assets/
   │       └───init.js
   ├───.gitignore
   ├───index.html
   ├───LICENSE
   ├───package.json
   └───README.md
```

## index.html

```
<!DOCTYPE html>
<html ng-app="demo" lang="en">
<head>
    <title>Demo application</title>

    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">

    <link rel="stylesheet" type="text/css" href="css/styles.css">
</head>
<body ng-controller="mainController">
	
    <div class="container">
        <h1>{ { heading } }</h1>
        <hr>
        <h2>{ { heading2 } }</h2>
    </div>

    <script src="js/scripts.js"></script>
</body>
</html>
```

## Gruntfile.js

```
module.exports = function(grunt) {
  grunt.initConfig({
    pkg: grunt.file.readJSON('package.json'),

    sass: {
      dist: {
        files: {
          'css/styles.css': 'css/src/main.scss'
        }
      }
    },

    cssmin: {
      options: {},
      target: {
        files: {
          'css/styles.css': [
            'css/src/assets/bootstrap.css',
            'css/styles.css'
          ]
        }
      }
    },

    uglify: {
      app: {
        options: {
          sourceMap: true
        },
        files: {
          'js/scripts.js': [
            'js/src/assets/angular.js',
            'js/src/init.js'
          ]
        }
      }
    },

    watch: {
      scripts: {
        files: ['js/src/*.js'],
        tasks: ['scripts'],
        options: {
          spawn: false,
        }
      },
      styles: {
        files: ['css/src/*.scss'],
        tasks: ['styles'],
        options: {
          spawn: false,
        }
      }
    }

  });


  grunt.loadNpmTasks('grunt-contrib-sass');
  grunt.loadNpmTasks('grunt-contrib-cssmin');
  grunt.loadNpmTasks('grunt-contrib-uglify-es');
  grunt.loadNpmTasks('grunt-contrib-watch');

  grunt.registerTask('styles', ['sass', 'cssmin']);
  grunt.registerTask('scripts', ['uglify']);

  grunt.registerTask('default', ['styles', 'scripts']);
  grunt.registerTask('develop', ['default', 'watch']);

};
```

## init.js

```
angular.module('demo', []);

angular.module('demo').controller('mainController', ['$scope', function($scope) {
    $scope.heading = 'Hello, world!';
    $scope.heading2 = 'My first angularJS application works!!!!!';
}]);
```
