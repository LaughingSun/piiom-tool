# piiom-tool library

Pixel Image Input, Output &amp; Memory tool library.  If you are looking for vector or model tools, this library may not suit your needs although it does support some texture formats and importing (and exporting) of vector image formats.

!!! Warning !!!

At this time this repository is just design / documentation / placeholder and contains no useful code or at most some testcases.

!!! end of Warning !!!

for usage information skip down to Installation, Usage or examples.

For support, bugs or contributing see support-and-contributing.md

For licensing you have 2 options: Either our MIT-license,d or commercial-license.md

For media, press and/or sponsorship please see media.md, press-kit.md and/or sponsorship.md

This page and the source code can be found at https://github.com/LaughingSun/piiom-tool.

Thank you for your interest!  If you can please support us by making a monetary contribution to this project (see sponsorship.md for details.)

# in depth

This tool library is specifically for pixel based file and memory formats and contains methods for reading from files, writing to files, structured memory dumping, structured memory manipulation, conversion to and from an extended raw format and analysis tools.  

It is not intended as a graphics library in the sense of various filters, rotations and manipulations.  

Iy's purpose is to enable basic reading and writing of image files so that a target software can focus on its own target features.  

It is our hope that piiom-tool library can be easily dropin / plugin for other projects.

## features

Following is a summary list of the key parts of the tool libraryy:
+ primary class interfaces
+ supporting class interfaces
+ image file / buffer / stream reader / writer interfaces
+ image buffer interface
+ analyzer interface
+ minimalist manipulation interface

# api design information

Find our API reference document at piiom-api-reference.md

# target image types

+ extended raw
+ bmp (and it's many variations)
+ png
+ jpg
+ gif
+ WebP



