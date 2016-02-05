new file

# How to set up a site.

## Create Jekyll Site

```jekyll new my-awesome-site```

## Set up Grunt

create a ```package.json``` and ```Gruntfile.js```

### Edit the package.json

Add this to the package.json file

```
{
  “name”: “my-site-name”,
  “description”: “My new Jekyll site.”,
  “version”: “0.1.0”,
  “devDependencies”: {
    “grunt”: “~0.4.5”,
    “grunt-contrib-watch”: “~0.6.1”,
    “grunt-shell”: “^1.1.2”,
    “load-grunt-tasks”: “~0.6.0”,
    “time-grunt”: “~0.4.0”
  }
}
```

Run ```npm install``` in the CLI. Grunt plugins get added to the node_modules folder.

Add ```exclude: [‘node_modules’]``` to the _config.yml so that node_modules does not get added to the site build.

### Edit the Grunt file

Stop Jekyll from building the css as Grunt will take over the task instead
```exclude: [‘css’, ‘_scss’]```

tell Jekyll not to erase the CSS directory in the _site output folder each time it rebuilds
```keep_files: [‘_site/css’]```

### Move the main.scss file and delete css folder

Out of the box, Jekyll has a separate CSS directory in the root of the project that contains the main.scss file. For simplicity sake, and because Jekyll no longer has to worry about the Sass files, I’ve moved main.scss into the _sass directory and gotten rid of the empty CSS directory. I recommend you do this as well so the upcoming Sass config path examples are consistent with your own.

## Remove front matter from main.scss so that Libsass can understand the file

## Load Grunt Plugins

```npm install grunt-concurrent grunt-sass —save-dev
```
grunt-concurrent, to allow tasks to run simultaneously, and grunt-sass, to run the node-sass compiler

## Run http://localhost:4000/

## Install Bootstrap

$ bower install bootstrap-sass

