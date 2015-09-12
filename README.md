# Carlos Cuesta Starter Kit

> A simple starterkit that I use to realize my front end static development projects. 

## Technologies 

- [**Gulp**](http://gulpjs.com) - Automate and enhance your workflow
- [**Jade**](http://jade-lang.com) - Terse language for writing HTML templates.
- [**SASS**](http://sass-lang.com) - CSS with superpowers.
- [**Babel**](https://babeljs.io) - Use next generation JavaScript, today (ES6 => ES5).
- [**NodeJS**](https://nodejs.org) - JavaScript runtime built on Chrome's V8 JavaScript engine.

## Requirements and Use 

### Requirements

- [Node.js](https://nodejs.org/en/)
- [Gulp](http://gulpjs.com)
```bash
$ npm install -g gulp
```

### Use 

```bash
$ git clone https://github.com/carloscuesta/starterkit.git
$ cd starterkit/ && npm install
$ gulp 
```

## Tasks

```gulp```: Runs the **default task** including the following tasks :

- ```scss```: SCSS compiling to CSS.
- ```jade```: Jade compiling and rendering to HTML.
- ```scripts```: ES6 to ES5 with babel, scripts minification and concatenation into a single file.
- ```image```: Image compression.
- ```browser-sync```: Starts a server at ```./dist/``` with all your compiled files, looking for file changes and injecting them into your browser.

```gulp deploy```: Deploy your ```dist``` folder into your server.

If you want to use the **deploy** task, you will have to edit the [```gulpfile.js```](https://github.com/carloscuesta/starterkit/blob/master/gulpfile.js#L48) lines between 48-54 with your ftp connection info: [```host```](https://github.com/carloscuesta/starterkit/blob/master/gulpfile.js#L51) | [```user```](https://github.com/carloscuesta/starterkit/blob/master/gulpfile.js#L52) | [```password```](https://github.com/carloscuesta/starterkit/blob/master/gulpfile.js#L53)

Once you setup ```ftpCredentials```, you will have to choose a directory of your server where the deploy will go: [```ftpUploadsDir```](https://github.com/carloscuesta/starterkit/blob/master/gulpfile.js#L44)

Now you will be able to use ```gulp deploy``` and your ```/dist/``` folder will go up to your ftp server!


## Project Structure

```
.
├── /dist/                   # Minified, optimized and compiled files.
│   ├── /assets/             # Assets folder.
│   │   ├── /css/            # CSS style files.
│   │   ├── /files/          # Static files.
│   │   │   └── img/         # Images folder.
│   │   └── /js/             # JS files.
│   └── *.html               # Rendered and compiled HTMLs from jade.
├── /node_modules/           # Node modules dependencies and packages.
├── /src/                    # Source files.
│   ├── /img/                # Images non compressed.
│   ├── /jade/               # Templating Jade files.
│   │   └── _includes/       # Templating Jade partials.
│   ├── /scss/               # SCSS style files.
│   │   └── _includes/       # Templating SCSS partials.
└── gulpfile.js              # Gulp automatization file.
```

## Screenshots

![gulp](https://cloud.githubusercontent.com/assets/7629661/9824378/ae8ade36-58cc-11e5-875a-86929fadb327.png)
![gulp-deploy](https://cloud.githubusercontent.com/assets/7629661/9824399/cece3d5a-58cc-11e5-9612-697e8a28b57b.png)


## License

The code is available under the [MIT](https://github.com/carloscuesta/starterkit/blob/master/LICENSE) license.