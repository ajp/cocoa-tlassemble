# tlassemble
tlassemble is a simple command line utility that combines a sequence of images into a movie. A GUI version, Time Lapse Assembler is available [here](http://www.dayofthenewdan.com/projects/time-lapse-assembler-1)

If you find this software useful, please consider making a small donation to fund future development.
[Donate now](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=9465YBPSUC9YL)

###Building and Installation
To build you must install XCode and the XCode developer tools.

```bash
$ git clone https://github.com/dbridges/cocoa-tlassemble.git
$ cd cocoa-tlassemble
$ make
$ sudo cp tlassemble /usr/local/bin/
```

###Usage
```bash
$ tlassemble INPUTDIRECTORY OUTPUTFILENAME [OPTIONS]
```

###Examples
```bash
$ tlassemble ./images time_lapse.mov
$ tlassemble ./images time_lapse.mov -fps 30 -height 720 -codec h264 -quality high
$ tlassemble ./images time_lapse.mov -quiet yes
```

###Options
```
-fps: Frames per second for final movie can be anywhere between 0.1 and 60.0.
-height: If specified images are resized proportionally to height given.
-codec: Codec to use to encode can be 'h264' 'photojpeg' 'raw' or 'mpv4'.
-quality: Quality to encode with can be 'high' 'normal' 'low'.
-quiet: Set to 'yes' to suppress output during encoding.
-reverse: Set to 'yes' to reverse the order that images are displayed in the movie.
```

###License
tlassemble can be distributed in accordance to the BSD New license. See the header in [tlassemble.m](https://github.com/dbridges/cocoa-tlassemble/blob/master/tlassemble.m) for full license terms.

