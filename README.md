# api documentation for  [vinyl-ftp (v0.6.0)](https://github.com/morris/vinyl-ftp#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-vinyl-ftp.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-vinyl-ftp) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-vinyl-ftp.svg)](https://travis-ci.org/npmdoc/node-npmdoc-vinyl-ftp)
#### Vinyl adapter for FTP

[![NPM](https://nodei.co/npm/vinyl-ftp.png?downloads=true)](https://www.npmjs.com/package/vinyl-ftp)

[![apidoc](https://npmdoc.github.io/node-npmdoc-vinyl-ftp/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-vinyl-ftp_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-vinyl-ftp/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-vinyl-ftp/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-vinyl-ftp/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Morris Brodersen",
        "email": "mb@morrisbrodersen.de",
        "url": "http://morrisbrodersen.de"
    },
    "bugs": {
        "url": "https://github.com/morris/vinyl-ftp/issues"
    },
    "dependencies": {
        "ftp": "^0.3.8",
        "minimatch": "^3.0.2",
        "object-assign": "^4.1.1",
        "parallel-transform": "^1.1.0",
        "through2": "^2.0.3",
        "vinyl": "^2.0.1"
    },
    "description": "Vinyl adapter for FTP",
    "devDependencies": {
        "istanbul": "^0.4.5",
        "mocha": "^3.2.0",
        "rmdir": "^1.2.0",
        "vinyl-fs": "^2.4.4"
    },
    "directories": {},
    "dist": {
        "shasum": "2fb43ec4d58a2e4c06b406e569cee9b3aa5df8ca",
        "tarball": "https://registry.npmjs.org/vinyl-ftp/-/vinyl-ftp-0.6.0.tgz"
    },
    "engines": {
        "node": ">=0.10.0"
    },
    "files": [
        "index.js",
        "lib"
    ],
    "gitHead": "dcb4d542984a11d137a5c6231a274bfce414a5fb",
    "homepage": "https://github.com/morris/vinyl-ftp#readme",
    "keywords": [
        "vinyl",
        "gulp",
        "ftp",
        "deploy",
        "deployment",
        "upload"
    ],
    "license": "MIT",
    "maintainers": [
        {
            "name": "morris4",
            "email": "mb@morrisbrodersen.de"
        }
    ],
    "name": "vinyl-ftp",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/morris/vinyl-ftp.git"
    },
    "scripts": {
        "test": "istanbul cover node_modules/mocha/bin/_mocha test"
    },
    "version": "0.6.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module vinyl-ftp](#apidoc.module.vinyl-ftp)
1.  [function <span class="apidocSignatureSpan">vinyl-ftp.</span>create ( config )](#apidoc.element.vinyl-ftp.create)
1.  object <span class="apidocSignatureSpan">vinyl-ftp.</span>filter
1.  object <span class="apidocSignatureSpan">vinyl-ftp.</span>ftp
1.  object <span class="apidocSignatureSpan">vinyl-ftp.</span>helpers
1.  object <span class="apidocSignatureSpan">vinyl-ftp.</span>mode

#### [module vinyl-ftp.filter](#apidoc.module.vinyl-ftp.filter)
1.  [function <span class="apidocSignatureSpan">vinyl-ftp.</span>filter ( folder, filter, options )](#apidoc.element.vinyl-ftp.filter.filter)
1.  [function <span class="apidocSignatureSpan">vinyl-ftp.filter.</span>differentSize ( folder, options )](#apidoc.element.vinyl-ftp.filter.differentSize)
1.  [function <span class="apidocSignatureSpan">vinyl-ftp.filter.</span>newer ( folder, options )](#apidoc.element.vinyl-ftp.filter.newer)
1.  [function <span class="apidocSignatureSpan">vinyl-ftp.filter.</span>newerOrDifferentSize ( folder, options )](#apidoc.element.vinyl-ftp.filter.newerOrDifferentSize)

#### [module vinyl-ftp.ftp](#apidoc.module.vinyl-ftp.ftp)
1.  [function <span class="apidocSignatureSpan">vinyl-ftp.ftp.</span>acquire ( cb )](#apidoc.element.vinyl-ftp.ftp.acquire)
1.  [function <span class="apidocSignatureSpan">vinyl-ftp.ftp.</span>chmod ( path, mode, cb )](#apidoc.element.vinyl-ftp.ftp.chmod)
1.  [function <span class="apidocSignatureSpan">vinyl-ftp.ftp.</span>downbuffer ( path, cb )](#apidoc.element.vinyl-ftp.ftp.downbuffer)
1.  [function <span class="apidocSignatureSpan">vinyl-ftp.ftp.</span>downstream ( path, cb )](#apidoc.element.vinyl-ftp.ftp.downstream)
1.  [function <span class="apidocSignatureSpan">vinyl-ftp.ftp.</span>list ( path, cb )](#apidoc.element.vinyl-ftp.ftp.list)
1.  [function <span class="apidocSignatureSpan">vinyl-ftp.ftp.</span>mkdirp ( path, cb )](#apidoc.element.vinyl-ftp.ftp.mkdirp)
1.  [function <span class="apidocSignatureSpan">vinyl-ftp.ftp.</span>mlsd ( path, cb )](#apidoc.element.vinyl-ftp.ftp.mlsd)
1.  [function <span class="apidocSignatureSpan">vinyl-ftp.ftp.</span>mlsdOrList ( path, cb )](#apidoc.element.vinyl-ftp.ftp.mlsdOrList)
1.  [function <span class="apidocSignatureSpan">vinyl-ftp.ftp.</span>pushIdle ( ftp )](#apidoc.element.vinyl-ftp.ftp.pushIdle)
1.  [function <span class="apidocSignatureSpan">vinyl-ftp.ftp.</span>release ( ftp, force )](#apidoc.element.vinyl-ftp.ftp.release)
1.  [function <span class="apidocSignatureSpan">vinyl-ftp.ftp.</span>reload ()](#apidoc.element.vinyl-ftp.ftp.reload)
1.  [function <span class="apidocSignatureSpan">vinyl-ftp.ftp.</span>remote ( path, cb )](#apidoc.element.vinyl-ftp.ftp.remote)
1.  [function <span class="apidocSignatureSpan">vinyl-ftp.ftp.</span>upload ( file, path, cb )](#apidoc.element.vinyl-ftp.ftp.upload)
1.  [function <span class="apidocSignatureSpan">vinyl-ftp.ftp.</span>vinylFiles ( dirname, files )](#apidoc.element.vinyl-ftp.ftp.vinylFiles)

#### [module vinyl-ftp.helpers](#apidoc.module.vinyl-ftp.helpers)
1.  [function <span class="apidocSignatureSpan">vinyl-ftp.helpers.</span>fixDate ( date )](#apidoc.element.vinyl-ftp.helpers.fixDate)
1.  [function <span class="apidocSignatureSpan">vinyl-ftp.helpers.</span>isDirectory ( vf )](#apidoc.element.vinyl-ftp.helpers.isDirectory)
1.  [function <span class="apidocSignatureSpan">vinyl-ftp.helpers.</span>join ()](#apidoc.element.vinyl-ftp.helpers.join)
1.  [function <span class="apidocSignatureSpan">vinyl-ftp.helpers.</span>log ()](#apidoc.element.vinyl-ftp.helpers.log)
1.  [function <span class="apidocSignatureSpan">vinyl-ftp.helpers.</span>makeOptions ( options )](#apidoc.element.vinyl-ftp.helpers.makeOptions)
1.  [function <span class="apidocSignatureSpan">vinyl-ftp.helpers.</span>normalize ( path )](#apidoc.element.vinyl-ftp.helpers.normalize)
1.  [function <span class="apidocSignatureSpan">vinyl-ftp.helpers.</span>parallel ( transform, options )](#apidoc.element.vinyl-ftp.helpers.parallel)

#### [module vinyl-ftp.mode](#apidoc.module.vinyl-ftp.mode)
1.  [function <span class="apidocSignatureSpan">vinyl-ftp.</span>mode ( folder, mode, options )](#apidoc.element.vinyl-ftp.mode.mode)



# <a name="apidoc.module.vinyl-ftp"></a>[module vinyl-ftp](#apidoc.module.vinyl-ftp)

#### <a name="apidoc.element.vinyl-ftp.create"></a>[function <span class="apidocSignatureSpan">vinyl-ftp.</span>create ( config )](#apidoc.element.vinyl-ftp.create)
- description and source-code
```javascript
create = function ( config ) {

	return new VinylFtp( config );

}
```
- example usage
```shell
...
'''javascript
var gulp = require( 'gulp' );
var gutil = require( 'gulp-util' );
var ftp = require( 'vinyl-ftp' );

gulp.task( 'deploy', function () {

	var conn = ftp.create( {
		host:     'mywebsite.tld',
		user:     'me',
		password: 'mypass',
		parallel: 10,
		log:      gutil.log
	} );
...
```



# <a name="apidoc.module.vinyl-ftp.filter"></a>[module vinyl-ftp.filter](#apidoc.module.vinyl-ftp.filter)

#### <a name="apidoc.element.vinyl-ftp.filter.filter"></a>[function <span class="apidocSignatureSpan">vinyl-ftp.</span>filter ( folder, filter, options )](#apidoc.element.vinyl-ftp.filter.filter)
- description and source-code
```javascript
filter = function ( folder, filter, options ) {

		options = this.makeOptions( options );
		var self = this;

		return this.parallel( function ( file, cb ) {

			var path = self.join( '/', folder, file.relative );

			self.remote( path, onRemote );

			function onRemote( err, remote ) {

				if ( err ) return cb( err );
				filter( file, remote, onFilter );

			}

			function onFilter( err, emit ) {

				cb( err, emit ? file : null );

			}

		}, options );

	}
```
- example usage
```shell
...
Returns a transform stream which filters the input for files
which have a different file size than their remote counterpart.

### conn.newerOrDifferentSize( remoteFolder[, options] ) <small>STREAM</small>

See above.

### conn.filter( remoteFolder, filter[, options] ) <small>STREAM</small>

Returns a transform stream that filters the input using a callback.
The callback should be of this form:

'''javascript
function ( localFile, remoteFile, callback ) {
...
```

#### <a name="apidoc.element.vinyl-ftp.filter.differentSize"></a>[function <span class="apidocSignatureSpan">vinyl-ftp.filter.</span>differentSize ( folder, options )](#apidoc.element.vinyl-ftp.filter.differentSize)
- description and source-code
```javascript
differentSize = function ( folder, options ) {

		options = this.makeOptions( options );
		return this.filter( folder, function ( file, remote, cb ) {

			cb( null, !remote || file.stat.size !== remote.ftp.size );

		}, options );

	}
```
- example usage
```shell
...
'mode' must be a string between '0000' and '0777'.

### conn.newer( remoteFolder[, options] ) <small>STREAM</small>

Returns a transform stream which filters the input for files
which are newer than their remote counterpart.

### conn.differentSize( remoteFolder[, options] ) <small>STREAM</small>

Returns a transform stream which filters the input for files
which have a different file size than their remote counterpart.

### conn.newerOrDifferentSize( remoteFolder[, options] ) <small>STREAM</small>

See above.
...
```

#### <a name="apidoc.element.vinyl-ftp.filter.newer"></a>[function <span class="apidocSignatureSpan">vinyl-ftp.filter.</span>newer ( folder, options )](#apidoc.element.vinyl-ftp.filter.newer)
- description and source-code
```javascript
newer = function ( folder, options ) {

		options = this.makeOptions( options );
		return this.filter( folder, function ( file, remote, cb ) {

			cb( null, !remote || file.stat.mtime > remote.ftp.date );

		}, options );

	}
```
- example usage
```shell
...
		'index.html'
	];

	// using base = '.' will transfer everything to /public_html correctly
	// turn off buffering in gulp.src for best performance

	return gulp.src( globs, { base: '.', buffer: false } )
		.pipe( conn.newer( '/public_html' ) ) // only upload newer files
		.pipe( conn.dest( '/public_html' ) );

} );
'''

Without Gulp:
...
```

#### <a name="apidoc.element.vinyl-ftp.filter.newerOrDifferentSize"></a>[function <span class="apidocSignatureSpan">vinyl-ftp.filter.</span>newerOrDifferentSize ( folder, options )](#apidoc.element.vinyl-ftp.filter.newerOrDifferentSize)
- description and source-code
```javascript
newerOrDifferentSize = function ( folder, options ) {

		options = this.makeOptions( options );
		return this.filter( folder, function ( file, remote, cb ) {

			cb( null, !remote || file.stat.mtime > remote.ftp.date || file.stat.size !== remote.ftp.size );

		}, options );

	}
```
- example usage
```shell
...
which are newer than their remote counterpart.

### conn.differentSize( remoteFolder[, options] ) <small>STREAM</small>

Returns a transform stream which filters the input for files
which have a different file size than their remote counterpart.

### conn.newerOrDifferentSize( remoteFolder[, options] ) <small>STREAM</small>

See above.

### conn.filter( remoteFolder, filter[, options] ) <small>STREAM</small>

Returns a transform stream that filters the input using a callback.
The callback should be of this form:
...
```



# <a name="apidoc.module.vinyl-ftp.ftp"></a>[module vinyl-ftp.ftp](#apidoc.module.vinyl-ftp.ftp)

#### <a name="apidoc.element.vinyl-ftp.ftp.acquire"></a>[function <span class="apidocSignatureSpan">vinyl-ftp.ftp.</span>acquire ( cb )](#apidoc.element.vinyl-ftp.ftp.acquire)
- description and source-code
```javascript
acquire = function ( cb ) {

		if ( this.idle.length > 0 ) {

			cb( null, this.idle.shift() );

		} else if ( this.connectionCount < this.config.maxConnections ) {

			this.log( 'CONN ' );

			var self = this;
			var ftp = new Ftp();
			var called = false;
			++this.connectionCount;

			ftp.on( 'ready', function () {

				self.log( 'READY' );
				called = true;
				cb( null, ftp );

			} );

			ftp.on( 'error', function ( err ) {

				var code = err.code ? (' (' + err.code + ')') : '';
				self.log( 'ERROR', err.stack + code );
				self.release( ftp, true );

				// only enqueue callback if not called yet
				if ( !called ) {

					called = true;

					if ( self.connectionCount === 0 ) {

						// there's no hope that a working connection will be released
						// pass error
						return cb( err );

					}

					self.queue.push( cb );

				}

			} );

			ftp.connect( this.config );

		} else {

			this.queue.push( cb );

		}

	}
```
- example usage
```shell
...
module.exports = del;

function del( path, cb ) {

	var self = this;
	var rel;

	this.acquire( onAcquire );

	function onAcquire( err, ftp ) {

		rel = ftp;
		if ( err ) return final( err );

		self.log( 'DEL  ', path );
...
```

#### <a name="apidoc.element.vinyl-ftp.ftp.chmod"></a>[function <span class="apidocSignatureSpan">vinyl-ftp.ftp.</span>chmod ( path, mode, cb )](#apidoc.element.vinyl-ftp.ftp.chmod)
- description and source-code
```javascript
chmod = function ( path, mode, cb ) {

		var self = this;
		path = this.join( '/', path );
		var rel;

		self.acquire( onAcquire );

		function onAcquire( err, ftp ) {

			rel = ftp;
			if ( err ) return final( err );

			self.log( 'SITE ', 'CHMOD', mode, path );
			ftp.site( 'CHMOD ' + mode + ' ' + path, final );

		}

		function final( err ) {

			self.release( rel );
			cb( err );

		}

	}
```
- example usage
```shell
...

		options = this.makeOptions( options );
		var self = this;

		var stream = this.parallel( function ( file, cb ) {

			var path = self.join( '/', folder, file.relative );
			self.chmod( path, mode, cb );

		}, options );

		stream.resume();
		return stream;

	}
...
```

#### <a name="apidoc.element.vinyl-ftp.ftp.downbuffer"></a>[function <span class="apidocSignatureSpan">vinyl-ftp.ftp.</span>downbuffer ( path, cb )](#apidoc.element.vinyl-ftp.ftp.downbuffer)
- description and source-code
```javascript
downbuffer = function ( path, cb ) {

		this.downstream( path, function ( err, stream ) {

			if ( err ) return cb( err );

			var bufs = [];

			stream.on( 'data', function ( data ) {

				bufs.push( data );

			} );

			stream.on( 'end', function () {

				cb( null, Buffer.concat( bufs ) );

			} );

			stream.on( 'error', function ( err ) {

				 cb( err );

			} );

		} );

	}
```
- example usage
```shell
...
	}

	if ( !options.read ) return glob;

	function getContents( file, cb ) {

		if ( self.isDirectory( file ) ) return cb( null, file );
		if ( options.buffer ) return self.downbuffer( file.path, onContents );
		self.downstream( file.path, onContents );

		function onContents( err, contents ) {

			if ( err ) return cb( err );
			file.contents = contents;
...
```

#### <a name="apidoc.element.vinyl-ftp.ftp.downstream"></a>[function <span class="apidocSignatureSpan">vinyl-ftp.ftp.</span>downstream ( path, cb )](#apidoc.element.vinyl-ftp.ftp.downstream)
- description and source-code
```javascript
downstream = function ( path, cb ) {

		var self = this;
		var remote, rel;

		this.remote( path, onRemote );

		function onRemote( err, rem ) {

			if ( err ) return cb( err );
			if ( !rem ) return cb( new Error( 'No such file' ) );
			remote = rem;

			self.acquire( onAcquire );

		}

		function onAcquire( err, ftp ) {

			rel = ftp;
			if ( err ) return onStream( err );

			self.log( 'GET  ', path );
			ftp.get( path, onStream );

		}

		function onStream( err, stream ) {

			if ( err ) {

				self.release( rel );
				return cb( err );

			}

			stream.on( 'end', function () {

				self.release( rel );

			} );

			stream.on( 'error', function () {

				self.release( rel, true );

			} );

			var bytes = 0;
			var size = remote.ftp.size;

			stream.on( 'data', function ( chunk ) {

				bytes += chunk.length;

				var progress = Math.floor( bytes / size * 100 ).toString();
				if ( progress.length === 1 ) progress = '  ' + progress;
				if ( progress.length === 2 ) progress = ' ' + progress;

				self.log( 'DOWN ', progress + '% ' + path );

			} );

			// the socket stream returned by the ftp client cannot be paused
			// add intermediate passthrough stream so piped streams get data
			stream = stream.pipe( new Stream.PassThrough() );

			cb( null, stream );

		}

	}
```
- example usage
```shell
...

		}

	},

	downbuffer: function ( path, cb ) {

		this.downstream( path, function ( err, stream ) {

			if ( err ) return cb( err );

			var bufs = [];

			stream.on( 'data', function ( data ) {
...
```

#### <a name="apidoc.element.vinyl-ftp.ftp.list"></a>[function <span class="apidocSignatureSpan">vinyl-ftp.ftp.</span>list ( path, cb )](#apidoc.element.vinyl-ftp.ftp.list)
- description and source-code
```javascript
list = function ( path, cb ) {

		if ( !this._list ) {

			var self = this;

			this._list = new Cache( function ( path, cb ) {

				var rel;

				self.acquire( onAcquire );

				function onAcquire( err, ftp ) {

					rel = ftp;
					if ( err ) return final( err );

					self.log( 'LIST ', path );
					ftp.list( path, onFiles );

				}

				function onFiles( err, files ) {

					// no such file or directory
					if ( err && ( err.code === 550 || err.code === 450 ) ) return final( null, [] );
					if ( err ) return final( err );

					final( null, self.vinylFiles( path, files ) );

				}

				function final( err, files ) {

					self.release( rel );
					cb( err, files );

				}

			} );

		}

		path = this.join( '/', path );
		this._list.get( path, cb );

	}
```
- example usage
```shell
...

	},

	mlsdOrList: function ( path, cb ) {

		var self = this;

		if ( this.noMlsd ) return this.list( path, cb );

		setImmediate(function() {
			self.mlsd( path, onMlsd );
		});

		function onMlsd( err, files ) {
...
```

#### <a name="apidoc.element.vinyl-ftp.ftp.mkdirp"></a>[function <span class="apidocSignatureSpan">vinyl-ftp.ftp.</span>mkdirp ( path, cb )](#apidoc.element.vinyl-ftp.ftp.mkdirp)
- description and source-code
```javascript
mkdirp = function ( path, cb ) {

		if ( !this._mkdirp ) {

			var self = this;

			this._mkdirp = new Cache( function ( path, cb ) {

				// skip if path is root
				if ( path === '/' || path === '' ) {

					return final();

				}

				self.remote( path, onRemote );

				function onRemote( err, remote ) {

					if ( err ) return final( err );
					if ( remote && !self.isDirectory( remote ) ) return final( new Error( path + ' is a file, cannot MKDIR' ) );
					if ( remote ) return final(); // skip if exists

					// ensure that parent directory exists
					self.mkdirp( Path.dirname( path ), onParent );

				}

				function onParent( err ) {

					if ( err ) return final( err );
					self.acquire( onAcquire );

				}

				var rel;

				function onAcquire( err, ftp ) {

					rel = ftp;
					if ( err ) return final( err );

					self.log( 'MKDIR', path );
					ftp.mkdir( path, final );

				}

				function final( err ) {

					self.release( rel );
					if ( err && err.message.match( /file exists/i ) ) return cb();
					cb( err );

				}

			} );

		}

		path = this.join( '/', path );
		return this._mkdirp.get( path, cb );

	}
```
- example usage
```shell
...
	upload: function ( file, path, cb ) {

		var self = this;
		var stream = new Stream.PassThrough();

		if ( file.isNull() ) {

			if ( file.stat && file.stat.isDirectory() ) this.mkdirp( path, cb );
			else cb( null, file );

			return;

		}

		if ( file.isStream() ) {
...
```

#### <a name="apidoc.element.vinyl-ftp.ftp.mlsd"></a>[function <span class="apidocSignatureSpan">vinyl-ftp.ftp.</span>mlsd ( path, cb )](#apidoc.element.vinyl-ftp.ftp.mlsd)
- description and source-code
```javascript
mlsd = function ( path, cb ) {

		if ( !this._mlsd ) {

			var self = this;

			this._mlsd = new Cache( function ( path, cb ) {

				var rel;

				self.acquire( onAcquire );

				function onAcquire( err, ftp ) {

					rel = ftp;
					if ( err ) return final( err );

					self.log( 'MLSD ', path );
					mlsd.bind( ftp )( path, onFiles );

				}

				function onFiles( err,  files ) {

					// no such file or directory
					if ( err && ( err.code === 501 || err.code === 550 ) ) return final( null, [] );
					if ( err ) return final( err );

					final( null, self.vinylFiles( path, files ) );

				}

				function final( err, files ) {

					self.release( rel );
					cb( err, files );

				}

			} );

		}

		path = this.join( '/', path );
		this._mlsd.get( path, cb );

	}
```
- example usage
```shell
...
	mlsdOrList: function ( path, cb ) {

		var self = this;

		if ( this.noMlsd ) return this.list( path, cb );

		setImmediate(function() {
			self.mlsd( path, onMlsd );
		});

		function onMlsd( err, files ) {

			if ( err && ( err.code === 502 || err.code === 500 ) ) {

				// mlsd not implemented, fallback to LIST
...
```

#### <a name="apidoc.element.vinyl-ftp.ftp.mlsdOrList"></a>[function <span class="apidocSignatureSpan">vinyl-ftp.ftp.</span>mlsdOrList ( path, cb )](#apidoc.element.vinyl-ftp.ftp.mlsdOrList)
- description and source-code
```javascript
mlsdOrList = function ( path, cb ) {

		var self = this;

		if ( this.noMlsd ) return this.list( path, cb );

		setImmediate(function() {
			self.mlsd( path, onMlsd );
		});

		function onMlsd( err, files ) {

			if ( err && ( err.code === 502 || err.code === 500 ) ) {

				// mlsd not implemented, fallback to LIST
				return self.list( path, cb );

			} else if ( files && files.length > 0 && !files[ 0 ].ftp.date ) {

				// mlsd didnt send any date, try LIST
				return self.list( path, cb );

			}

			cb( err, files );

		}

	}
```
- example usage
```shell
...
	remote: function ( path, cb ) {

		var self = this;
		path = this.join( '/', path );
		var basename = Path.basename( path );
		var dirname = Path.dirname( path );

		self.mlsdOrList( dirname, onFiles );

		function onFiles( err, files ) {

			if ( err ) return cb( err );

			for ( var i = 0; i < files.length; ++i ) {
...
```

#### <a name="apidoc.element.vinyl-ftp.ftp.pushIdle"></a>[function <span class="apidocSignatureSpan">vinyl-ftp.ftp.</span>pushIdle ( ftp )](#apidoc.element.vinyl-ftp.ftp.pushIdle)
- description and source-code
```javascript
pushIdle = function ( ftp ) {

		var self = this;

		// add connection to idle list
		this.idle.push( ftp );

		// reset any earlier timeout
		clearTimeout( this.idleTimer );

		// disconnect all after timeout
		this.idleTimer = setTimeout( function () {

			self.idle.forEach( function ( ftp ) {

				self.log( 'DISC ' );
				ftp.end();
				--self.connectionCount;

			} );

			self.idle = [];

		}, this.config.idleTimeout );

	}
```
- example usage
```shell
...

			reuse = true;
			var first = this.queue.shift();
			first( null, ftp );

		} else {

			this.pushIdle( ftp );

		}

	},

	reload: function () {
...
```

#### <a name="apidoc.element.vinyl-ftp.ftp.release"></a>[function <span class="apidocSignatureSpan">vinyl-ftp.ftp.</span>release ( ftp, force )](#apidoc.element.vinyl-ftp.ftp.release)
- description and source-code
```javascript
release = function ( ftp, force ) {

		if ( !ftp ) return;

		if ( force ) {

			this.log( 'DISC ' );
			ftp.end();
			--this.connectionCount;

		} else if ( this.queue.length > 0 ) {

			reuse = true;
			var first = this.queue.shift();
			first( null, ftp );

		} else {

			this.pushIdle( ftp );

		}

	}
```
- example usage
```shell
...
		self.log( 'DEL  ', path );
		ftp.delete( path, final );

	}

	function final( err ) {

		self.release( rel );
		cb( err );

	}

}
...
```

#### <a name="apidoc.element.vinyl-ftp.ftp.reload"></a>[function <span class="apidocSignatureSpan">vinyl-ftp.ftp.</span>reload ()](#apidoc.element.vinyl-ftp.ftp.reload)
- description and source-code
```javascript
reload = function () {

		if ( this._mkdirp ) this._mkdirp.clear();
		if ( this._mlsd ) this._mlsd.clear();
		if ( this._list ) this._list.clear();

		return this;

	}
```
- example usage
```shell
...
		return stream;

	},

	makeOptions: function ( options ) {

		options = options || {};
		if ( options.reload ) this.reload();
		return options;

	},

	fixDate: function ( date ) {

		if ( !date ) return null;
...
```

#### <a name="apidoc.element.vinyl-ftp.ftp.remote"></a>[function <span class="apidocSignatureSpan">vinyl-ftp.ftp.</span>remote ( path, cb )](#apidoc.element.vinyl-ftp.ftp.remote)
- description and source-code
```javascript
remote = function ( path, cb ) {

		var self = this;
		path = this.join( '/', path );
		var basename = Path.basename( path );
		var dirname = Path.dirname( path );

		self.mlsdOrList( dirname, onFiles );

		function onFiles( err, files ) {

			if ( err ) return cb( err );

			for ( var i = 0; i < files.length; ++i ) {

				if ( files[ i ].ftp.name === basename ) return cb( null, files[ i ] );

			}

			cb();

		}

	}
```
- example usage
```shell
...
		options = this.makeOptions( options );
		var self = this;

		return this.parallel( function ( file, cb ) {

			var path = self.join( '/', folder, file.relative );

			self.remote( path, onRemote );

			function onRemote( err, remote ) {

				if ( err ) return cb( err );
				filter( file, remote, onFilter );

			}
...
```

#### <a name="apidoc.element.vinyl-ftp.ftp.upload"></a>[function <span class="apidocSignatureSpan">vinyl-ftp.ftp.</span>upload ( file, path, cb )](#apidoc.element.vinyl-ftp.ftp.upload)
- description and source-code
```javascript
upload = function ( file, path, cb ) {

		var self = this;
		var stream = new Stream.PassThrough();

		if ( file.isNull() ) {

			if ( file.stat && file.stat.isDirectory() ) this.mkdirp( path, cb );
			else cb( null, file );

			return;

		}

		if ( file.isStream() ) {
			file.contents.pipe( stream );
		} else if ( file.isBuffer() ) {
			stream.end( file.contents );
		}

		// ensure that parent directory exists
		self.mkdirp( Path.dirname( path ), onParent );

		function onParent( err ) {

			if ( err ) return final( err );
			self.acquire( onAcquire );

		}

		var rel;

		function onAcquire( err, ftp ) {

			rel = ftp;
			if ( err ) return final( err );

			self.log( 'PUT  ', path );
			ftp.put( stream, path, final );

			// THE FOLLOWING MUST BE AFTER ftp.put()
			// Somehow, if you attach a 'data' handler before
			// ftp.put, the callback of ftp.put is never called

			if ( file.stat ) {

				var uploaded = 0;
				var size = file.stat.size;

				stream.on( 'data', function ( chunk ) {

					uploaded += chunk.length;

					var progress = Math.floor( uploaded / size * 100 ).toString();
					if ( progress.length === 1 ) progress = '  ' + progress;
					if ( progress.length === 2 ) progress = ' ' + progress;

					self.log( 'UP   ', progress + '% ' + path );

				} );

			}

		}

		function final( err ) {

			self.release( rel );
			cb( err, file );

		}

	}
```
- example usage
```shell
...

	options = this.makeOptions( options );
	var self = this;

	var stream = this.parallel( function ( file, cb ) {

		var path = self.join( '/', folder, file.relative );
		self.upload( file, path, cb );

	}, options );

	stream.resume();
	return stream;

}
...
```

#### <a name="apidoc.element.vinyl-ftp.ftp.vinylFiles"></a>[function <span class="apidocSignatureSpan">vinyl-ftp.ftp.</span>vinylFiles ( dirname, files )](#apidoc.element.vinyl-ftp.ftp.vinylFiles)
- description and source-code
```javascript
vinylFiles = function ( dirname, files ) {

		var self = this;

		return files.filter( function ( file ) {

			return file.name !== '.' && file.name !== '..';

		} ).map( function ( file ) {

			file.date = self.fixDate( file.date );

			var vinyl = new Vinyl( {
				cwd: '/',
				path: self.join( dirname, file.name )
			} );
			vinyl.ftp = file;

			return vinyl;

		} );

	}
```
- example usage
```shell
...

				function onFiles( err,  files ) {

					// no such file or directory
					if ( err && ( err.code === 501 || err.code === 550 ) ) return final( null, [] );
					if ( err ) return final( err );

					final( null, self.vinylFiles( path, files ) );

				}

				function final( err, files ) {

					self.release( rel );
					cb( err, files );
...
```



# <a name="apidoc.module.vinyl-ftp.helpers"></a>[module vinyl-ftp.helpers](#apidoc.module.vinyl-ftp.helpers)

#### <a name="apidoc.element.vinyl-ftp.helpers.fixDate"></a>[function <span class="apidocSignatureSpan">vinyl-ftp.helpers.</span>fixDate ( date )](#apidoc.element.vinyl-ftp.helpers.fixDate)
- description and source-code
```javascript
fixDate = function ( date ) {

		if ( !date ) return null;

		var offset = 0;

		if ( this.config.timeOffset ) offset += this.config.timeOffset * 60000;

		return new Date( date.valueOf() + offset );

	}
```
- example usage
```shell
...

		return files.filter( function ( file ) {

			return file.name !== '.' && file.name !== '..';

		} ).map( function ( file ) {

			file.date = self.fixDate( file.date );

			var vinyl = new Vinyl( {
				cwd: '/',
				path: self.join( dirname, file.name )
			} );
			vinyl.ftp = file;
...
```

#### <a name="apidoc.element.vinyl-ftp.helpers.isDirectory"></a>[function <span class="apidocSignatureSpan">vinyl-ftp.helpers.</span>isDirectory ( vf )](#apidoc.element.vinyl-ftp.helpers.isDirectory)
- description and source-code
```javascript
isDirectory = function ( vf ) {

		return vf.ftp.type.match( /^d|dir/i );

	}
```
- example usage
```shell
...

	function check( err, remote, stats, cb ) {

		var method;

		if ( err ) {
			if ( err.message.match( /ENOENT/ ) ) {
				if ( self.isDirectory( remote ) ) {
					method = 'rmdir';
				} else {
					method = 'delete';
				}
			} else {
				return cb( err );
			}
...
```

#### <a name="apidoc.element.vinyl-ftp.helpers.join"></a>[function <span class="apidocSignatureSpan">vinyl-ftp.helpers.</span>join ()](#apidoc.element.vinyl-ftp.helpers.join)
- description and source-code
```javascript
join = function () {

		return Path.join.apply( Path, arguments ).replace( RE_BS, '/' );

	}
```
- example usage
```shell
...
	options = this.makeOptions( options );
	var self = this;

	var glob = this.glob( globs, options );

	function stat( remote, cb ) {

		Fs.stat( Path.join( local, remote.relative ), function ( err, stats ) {
			check( err, remote, stats, cb );
		} );

	}

	function check( err, remote, stats, cb ) {
...
```

#### <a name="apidoc.element.vinyl-ftp.helpers.log"></a>[function <span class="apidocSignatureSpan">vinyl-ftp.helpers.</span>log ()](#apidoc.element.vinyl-ftp.helpers.log)
- description and source-code
```javascript
log = function () {

		var log = this.config.log;

		if ( typeof log === 'function' ) log.apply( undefined, arguments );

	}
```
- example usage
```shell
...
	this.acquire( onAcquire );

	function onAcquire( err, ftp ) {

		rel = ftp;
		if ( err ) return final( err );

		self.log( 'DEL  ', path );
		ftp.delete( path, final );

	}

	function final( err ) {

		self.release( rel );
...
```

#### <a name="apidoc.element.vinyl-ftp.helpers.makeOptions"></a>[function <span class="apidocSignatureSpan">vinyl-ftp.helpers.</span>makeOptions ( options )](#apidoc.element.vinyl-ftp.helpers.makeOptions)
- description and source-code
```javascript
makeOptions = function ( options ) {

		options = options || {};
		if ( options.reload ) this.reload();
		return options;

	}
```
- example usage
```shell
...
var Fs = require( 'fs' );
var Path = require( 'path' );

module.exports = clean;

function clean( globs, local, options ) {

	options = this.makeOptions( options );
	var self = this;

	var glob = this.glob( globs, options );

	function stat( remote, cb ) {

		Fs.stat( Path.join( local, remote.relative ), function ( err, stats ) {
...
```

#### <a name="apidoc.element.vinyl-ftp.helpers.normalize"></a>[function <span class="apidocSignatureSpan">vinyl-ftp.helpers.</span>normalize ( path )](#apidoc.element.vinyl-ftp.helpers.normalize)
- description and source-code
```javascript
normalize = function ( path ) {

		return Path.normalize( path ).replace( RE_BS, '/' );

	}
```
- example usage
```shell
...

		return vf.ftp.type.match( /^d|dir/i );

	},

	normalize: function ( path ) {

		return Path.normalize( path ).replace( RE_BS, '/' );

	},

	join: function () {

		return Path.join.apply( Path, arguments ).replace( RE_BS, '/' );
...
```

#### <a name="apidoc.element.vinyl-ftp.helpers.parallel"></a>[function <span class="apidocSignatureSpan">vinyl-ftp.helpers.</span>parallel ( transform, options )](#apidoc.element.vinyl-ftp.helpers.parallel)
- description and source-code
```javascript
parallel = function ( transform, options ) {

		options = assign( {}, this.config, options );
		var p = Math.max( 1, parseInt( options.parallel ) );
		var stream = parallel( p, transform );

		return stream;

	}
```
- example usage
```shell
...
		if ( method ) {
			self[ method ]( remote.path, cb );
		} else {
			cb();
		}
	}

	return glob.pipe( this.parallel( stat, options ) );

}
...
```



# <a name="apidoc.module.vinyl-ftp.mode"></a>[module vinyl-ftp.mode](#apidoc.module.vinyl-ftp.mode)

#### <a name="apidoc.element.vinyl-ftp.mode.mode"></a>[function <span class="apidocSignatureSpan">vinyl-ftp.</span>mode ( folder, mode, options )](#apidoc.element.vinyl-ftp.mode.mode)
- description and source-code
```javascript
mode = function ( folder, mode, options ) {

		options = this.makeOptions( options );
		var self = this;

		var stream = this.parallel( function ( file, cb ) {

			var path = self.join( '/', folder, file.relative );
			self.chmod( path, mode, cb );

		}, options );

		stream.resume();
		return stream;

	}
```
- example usage
```shell
...

### conn.dest( remoteFolder[, options] ) <small>STREAM</small>

Returns a transform stream that transfers input files to a remote folder.
All directories are created automatically.
Passes input files through.

### conn.mode( remoteFolder, mode[, options] ) <small>STREAM</small>

Returns a transform stream that sets remote file permissions for each file.
'mode' must be a string between '0000' and '0777'.

### conn.newer( remoteFolder[, options] ) <small>STREAM</small>

Returns a transform stream which filters the input for files
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
