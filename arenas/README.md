Arenas
==================

Arenas are a crucial part of experimental design using the ethoscope platform.

An arena is physical translation of an experimental paradigm.

With the ethoscope platform, it is possible to work with multiple arenas according to your biological question and model organism.

Arenas are generally 3d printed and can be derived from templates.
Template arena have the suffix **"template"**

There are several conventional sizes of arena that corresponds to the camera mode of the ethoscopes.
namely, the sizes:

* standard 
* *mini* (the keyword mini is in the name of these arenas)

The mini arenas have smaller surfaces and are optimises for HD video acquisition.
The standard size is a good compromise between image surface and time resolution allowing users to perform real time tracking

Adding new arenas
--------------------------

When adding new arena. Please, provide:

* A README with a description (and and name, author, number of rois,...)
* An stl file
* A 1min mp4 video of the arena with animals. It can be done with `ffmpeg` (e.g. `ffmpeg -ss 00:01:00 -i input.mp4  -t 00:01:00  -c:v libx264 -preset veryslow -crf 26  arena_xxx_xxx.mp4`)



 
 

