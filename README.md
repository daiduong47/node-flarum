# node-flarum


[![Build Status](https://travis-ci.org/FlarumJS/node-flarum.svg?branch=master)](https://travis-ci.org/FlarumJS/node-flarum) [![GitHub version](https://badge.fury.io/gh/FlarumJS%2Fnode-flarum.svg)](https://badge.fury.io/gh/FlarumJS%2Fnode-flarum) [![NPM version](https://badge.fury.io/js/node-flarum.svg)](https://badge.fury.io/js/node-flarum)

A forum made out of [Flarum](http://flarum.org)'s design forum with NodeJS

## Installation

```sh
npm install node-flarum --save
```

## Usage

### HTTP

Using the http package required the following modules to be installed: *connect* & *connect-hopeful-body-parser*

```node
var http = require('http');
var connect = require('connect');
var bodyParser = require('connect-hopeful-body-parser');

var flarum = require('./index');

var app = connect();

app.use(bodyParser());
app.use(flarum); // You can only have flarum in root path, otherwise won't work

http.createServer(app).listen(8080);
```

### Express

```node
var flarum = require('node-flarum');

var express = require('express');
var app = express();

// Other stuff

app.use('/forum', flarum) // This will execute flarum on the "/forum" path
app.use(flarum)           // This will execute flarum on the root path
```



## Contributing

Whenever this forum is complete [•••], there will be a website here for the official *NodeJS* Flarum forum


## Release History

* v0.0.1-beta.1 - NPM Package Information
* v0.0.1.beta.2 - Added Configuration Tweaks, fixed links and mongodb problems ([Full Release Information](https://github.com/FlarumJS/node-flarum/releases/tag/v0.0.1-beta.2))
* v0.0.1-beta.3 - Added Sign Up & Log In Options ([Full Release Information](https://github.com/FlarumJS/node-flarum/releases/tag/v0.0.1-beta.3))
