# piiom-tool library
Pixel Image Input, Output &amp; Memory tool library.

!!! Warning !!!

At this time this repository is just design / documentation / placeholder and contains no useful code or at most some testcases.

!!! end of Warning !!!

This tool library is specifically for pixel based file and memory formats and contains methods for reading from files, writing to files, structured memory dumping, structured memory manipulation, conversion to and from an extended raw format and analysis tools.  It is not intended as a graphics library in the sense of various filters, rotations and manipulations.  The purpose is to enable basic reading and writing of image files so that a target software can focus on its own target features.  It is our hope that piiom-tool library can be easily dropin / plugin for other projects.

# features

There are basically 5 parts to the tool library, namely:
+ supporting class interfaces
+ image file / buffer / stream reader / writer interfaces
+ image buffer interface
+ analyzer interface
+ minimal manipulation interface

Assuming:
`const piiom = require( 'piiom' );`

## piiom module class interfaces



### class piiom.Reader interface

An interface for reading image data.



### class piiom.Writer interface

An interface for writing

### class piiom.Image interface

An interface for image data



### class piiom.Stream interface

An interface for reading image data.



## piiom module supporting class interfaces



### piiom.piiomEvent

A Event object used with listeners and event handling.


## piiom module methods

### piiom.createReader( source, options? )

returns a piiomReader instance or false on failure. see the piionReader class

argument  | type(s)         | default   | description
--------- | --------------- | --------- |------------------------------
source    | string          |           | path of file to be read
          | integer         |           | https://nodejs.org/api/all.html#fs_event_open
          | stream.Readable |           | https://nodejs.org/api/stream.html#stream_class_stream_readable
          | buffer          |           | https://nodejs.org/api/buffer.html#buffer_class_buffer
options   | object          |           | see the piionReader class constructor

### piiom.createWriter( target, options? )

returns a piiomWriter instance or false on failure. see the piionReader class

argument  | type(s)         | default   | description
--------- | --------------- | --------- |------------------------------
target    | string          |           | path of file to be written
          | integer         |           | https://nodejs.org/api/all.html#fs_event_open
          | stream.Readable |           | https://nodejs.org/api/stream.html#stream_class_stream_readable
          | buffer          |           | https://nodejs.org/api/buffer.html#buffer_class_buffer
options   | object          | { }       | see the piionWriter class constructor

piiom.createReader( source:{path-string|buffer|readable-file-handler|readable-stream}, options?:{object} ):{piiomReader|false}:{piiomReader|false}
piiom.createWriter( source:{path-string|buffer|writable-file-handler|writable-stream}, options?:{object} ):{piiomReader|false}:{piiomReader|false}

piiomReader#addListener( type:{string|event|array}, callback, options?:{object|integer} )
piiomReader#appendListener( type:{string|event|array}, callback, options?:{object|integer} ):{piiomEvent#|false}
piiomReader#prependListener( type:{string|event|array}, callback, options?:{object|integer} )
piiomReader#on( type:{string|event|array}, callback, options?:{object|integer} )
piiomReader#once( type:{string|event|array}, callback, options?:{object} )
piiomReader#remove( type:{string|event|array}, callback )
piiomReader#emit( type:{string|event|array} )

## Image file / stream reading interface

piiom.createReader( source:{path-string|buffer|file-handler|read-stream}, options?:{object} ):{piiomReader|false}:{piiomReader|false}

piiomReader#addListener( type:{string|event|array}, callback, options?:{object|integer} )
piiomReader#appendListener( type:{string|event|array}, callback, options?:{object|integer} ):{piiomEvent#|false}
piiomReader#prependListener( type:{string|event|array}, callback, options?:{object|integer} )
piiomReader#on( type:{string|event|array}, callback, options?:{object|integer} )
piiomReader#once( type:{string|event|array}, callback, options?:{object} )
piiomReader#remove( type:{string|event|array}, callback )
piiomReader#emit( type:{string|event|array} )

## Image file / stream / buffer writing interface

@TODO: give details


## Image buffer interface

@TODO: give details

## Image analyzer interface

@TODO: give details

## Image minimal manipulation interface

@TODO: give details

# target image types

+ extended raw
+ bmp (and it's many variations)
+ png
+ jpg
+ gif
+ WebP



