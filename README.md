Convert a folder of images to an animation

If using PowerPoint 2016 you can save all slides as images to be used as input

Use settings.conf or command line arguments to configure the input/output/etc

Install with 
`pip install imagestoanimation` 


Usage:

```
imgvid [-h] [-s SETTINGS] [-d DIRECTORY] [-f FILEFORMAT] [-c CODEC]
              [-o OUTPUT] [-r RATE] [-W WIDTH] [-H HEIGHT]

Args that start with '--' (eg. -d) can also be set in a config file (*.conf or
specified via -s). Config file syntax allows: key=value, flag=true,
stuff=[a,b,c] (for details, see syntax at https://goo.gl/R74nmi). If an arg is
specified in more than one place, then commandline values override config file
values which override defaults.

optional arguments:
  -h, --help            show this help message and exit
  -s SETTINGS, --settings SETTINGS
                        Config file path, usually *.conf
  -d DIRECTORY, --directory DIRECTORY
                        Directory containing frame files
  -f FILEFORMAT, --fileformat FILEFORMAT
                        Naming convention for frame files
  -c CODEC, --codec CODEC
                        Codec as FOURCC, see http://www.fourcc.org/codecs.php
  -o OUTPUT, --output OUTPUT
                        Output file name
  -r RATE, --rate RATE  Frames Per Second
  -W WIDTH, --width WIDTH
                        Output frame width
  -H HEIGHT, --height HEIGHT
                        Output frame height

```

Example:
```
imgvid -d="input" -f=Slide[0-9]*.PNG -c=XVID -o=output.avi -r=15 -w=1280 -h=720
```

