# piiom-tool library api reference document

Assuming:
`const piiom = require( 'piiom' );`

## piiom module class interfaces



### class piiom.Reader interface implements piiom.Stream

An interface for reading image data.



### class piiom.Writer interface implements piiom.Stream

An interface for writing

### class piiom.Image interface implements piiom.supporters.EventTarget

An interface for image data



### class piiom.Stream interface implements piiom.supporters.EventTarget

An interface for tranforming / transfering image data.



## piiom module supporting class interfaces



### piiom.supporting.EventTarget

A target that supports event object used with listeners and event handling.



### piiom.supporting.Event

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


piiomReader#addListener( type:{string|event|array}, callback, options?:{object|integer} )
piiomReader#appendListener( type:{string|event|array}, callback, options?:{object|integer} ):{piiomEvent#|false}
piiomReader#prependListener( type:{string|event|array}, callback, options?:{object|integer} )
piiomReader#on( type:{string|event|array}, callback, options?:{object|integer} )
piiomReader#once( type:{string|event|array}, callback, options?:{object} )
piiomReader#remove( type:{string|event|array}, callback )
piiomReader#emit( type:{string|event|array} )

## Image file / stream reading interface

@TODO: give details


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



