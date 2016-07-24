<div align="center">
    <div><img src="https://raw.githubusercontent.com/mattbierner/allthecolors.gif/master/documentation/array-smooth.png" /></div>
    <h1>allthecolors.gif</h1>
</div>

Collection of gifs which contain every [24-bit RGB color](https://en.wikipedia.org/wiki/Color_depth#True_color_.2824-bit.29).


### [rainbow-array.gif](https://dl.dropboxusercontent.com/s/skuaud9x4ss447m/rainbow-array.gif?dl=0)

* Each frame is **16 by 16 pixels** (256 colors per frame).
* Gif has **65535 frames**, each lasting 5 hundredths of a second (25fps). The entire animation lasts a little under **44 minutes**.
* Colors increase by counting from `0x000000` to `0xffffff`.
* File size is abut **70MB**.

### [rainbow-stack.gif](https://dl.dropboxusercontent.com/s/96nypblxn2kh4ak/rainbow-stack.gif?dl=0)

* Each frame is **2 by 1 pixels**. There are two colors stored per frame. (Why two instead of one? Well, two is the minimum size of a local color table in a gif.)
* Contains **8,388,608 frames**, each lasting 5 hundredths of a second (25fps). The entire animation lasts around **93 hours**.
* Colors on the left side count up `0x000000` to `0x800000`, while the colors on the right side count down from `0xffffff` to `0x800000`. 
* File size is abut **250MB**.


### [rainbow-stack-walk.gif](https://dl.dropboxusercontent.com/s/hbk7dats08f7mfb/rainbow-stack-walk.gif?dl=0)

Same as `rainbow-stack.gif`, but treats RGB space as a cube and uses a space filling Hilbert curve to choose which colors to go to. Starts at either end of the curve and works inwards. This eliminates the jarring transitions seen in the other methods.


# Viewing
In order to save space (ha!), all the included gif are very small and must be upscaled to view. When upscaling, most programs will automatically smooth out the resulting image:

![](https://raw.githubusercontent.com/mattbierner/allthecolors.gif/master/documentation/stack-smooth.png)

This is fine for `rainbow-array`, but you can instead use nearest neighbor upscaling for a more [Josef Albers-esque](https://en.wikipedia.org/wiki/Josef_Albers) experience:

![](https://raw.githubusercontent.com/mattbierner/allthecolors.gif/master/documentation/stack-pixelated.png)


These gifs are also too awesome for some image viewers to handle so don't be surprised if you see crashes or hangs while loading them.