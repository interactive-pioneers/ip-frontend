# iptools-frontend
Combined frontend setup for web projects consisting of the [generator-pioneerscss](https://www.npmjs.com/package/generator-pioneerscss) inuitcss setup and the [iptools-utils](https://github.com/interactive-pioneers/iptools-utils) Javascript utilities


## Getting Started

1. Move to your app folder, for example:

        $ cd ~/projects/my-app

2. Install [Yeoman](http://yeoman.io/) and the iptools-frontend:

        $ npm i yo iptools-frontend
        
3. Move to folder in which SCSS structure should be created at, e.g.:

        $ cd styles     

4. Scaffold structure via the included generator by running:

        $ yo pioneerscss
       
5. Include iptools-utils.js from the included iptools-utils package as a dependency in your Javascript build process.

6. Include the generated styles.scss and iptools-utils.scss from the included iptools-utils package in your CSS build process. An example is given below.


## CSS build task example

Grunt task for [grunt-sass](https://github.com/sindresorhus/grunt-sass):
```
var config = {
  src: 'src',
  dist: 'dist'
};
 
sass: {
  options: {
    outputStyle: 'expanded',
    includePaths: ['node_modules'],
    sourceMap: false
  },
  dist: {
    files: {
      '<%= config.dist %>/assets/css/styles.css': [
        '<%= config.src %>/assets/css/styles.scss',
        'node_modules/iptools-utils/src/iptools-utils.scss'
      ]
    }
  }
}
```

## Licence

Copyright © 2018 Interactive Pioneers GmbH. Licenced under [GPL-3](LICENSE).
