# ip-frontend
All-in-one frontend setup for Interactive Pioneers projects, consisting of SCSS and Javascript packages


## Getting Started

1. Install Yeoman and SCSS generator:

        $ npm i -g yo generator-pioneerscss

2. Move to folder in which SCSS structure should be created at, e.g.:

        $ cd ~/projects/my-app/styles

3. Scaffold structure by running:

        $ yo pioneerscss


## typical usage

Grunt task for [grunt-sass](https://github.com/sindresorhus/grunt-sass):
```
sass: {
  options: {
    outputStyle: 'expanded',
    includePaths: ['node_modules'],
    sourceMap: false
  },
  dist: {
    files: {
      '<%= config.dist %>/assets/css/styles.css': '<%= config.src %>/assets/css/styles.scss'
    }
  }
}
```
