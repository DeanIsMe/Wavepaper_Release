# Wavepaper
Wavepaper is a highly customisable image generator that simulates wave interference patterns to produce abstract art for wallpapers, or any other purpose. You can share configuration files, edit others' designs and generate images in ANY resolution!

### UI
(yes, it's clunky) 
![Wavepaper GUI](/thumbnails/Wavepaper_GUI.jpg)  

### Example wallpapers
<div>
<img src="/thumbnails/Contour.jpg" alt="Contour" width="49%"/>
<img src="/thumbnails/Insignia.jpg" alt="Insignia" width="49%"/>
</div>
<div>
<img src="/thumbnails/Wave Fronts.jpg" alt="Wave Fronts" width="49%"/>
<img src="/thumbnails/Star.jpg" alt="Star" width="49%"/>
</div>

### Installation

Run the installer. Note that this program requires the MATLAB runtime v8.5 (R2015a). If you don't have this MATLAB runtime, the installer will download and install it.  

Note that a more recent version of Wavepaper exists, written in C++ on Qt. It can be run without installation, but far less mature than this MATLAB version.  See it [here](https://github.com/DeanIsMe/Wavepaper_Qt).

### How do I make pretty pictures?

Click ALL THE THINGS!
Try 'Randomise'
Load example configurations and fiddle with them.

### The terminology

Waves are emitted from **Emitters**.  
One or more **Emitters** make a **Set**.  
One or more **Sets** make a **Phasor Field**.  
One or more **Phasor Fields** produce the **Output**.  

Apricot panels modify the current Set.  
Blue panels modify the current Phasor Field.  
Green panels modify the Output.  
 
To have multiple sets, click the 'Add Set' button, which will save the emitter locations of emitters you're currently modifying, and allow you to add another. 
The same system works for phasor fields. However, adding multiple phasor fields is for more advanced functions.

### Ripple settings

Enabling ripple applies a function to the colour map, 'removing' regions of the output. The modifying function is plotted.
As a general rule, try large numbers of ripples for large wavelengths, and small numbers of ripples for small wavelengths.

### Energiser settings

With the energiser disabled, each emitter produces waves independently. With the energiser enabled, the power and phase of each emitter is controlled by the distance from the energiser.
The location of the energiser will be visible as a large circle when this panel is open.

### Configuration files

You can save the config file at any time, which is a file that specifies the current state of your window. You can load this at a later time to modify, or share it with others. Whenever you export an image, a config file is also saved. This is especially useful when you want to re-generate the image at a different resolution.

### Computer resources

If you put a crazy number of emitters in the image (hundreds+), your computer may take a huge amount of time to process it.
Exporting a very high resolution image will consume a LOT of RAM (~6 GB for 13 MP). Try the 'Low RAM' option in the resolution panel if you're having issues. It has never happened to me, but I accept no responsibility for crashed computers.

### But how does it work?

If you really want to know, this is a wave physics simulation. For each point on the 2D plane, the phasor value from each emitter is calculated, and these phasors are added together. The waves will constructively or destructively interfere at different locations. The picture that you see is the logarithmically scaled resultant phasor magnitude (wave amplitude) represented by a colour map. You can actually  show the wave behaviour by simulating a single slit diffraction pattern - make a linear set of ~100 emitters with the total length of about 2 wavelengths. All clear? No? Doesn't matter, the point is pretty pictures.

The simulation functionality was originally written for my undergraduate thesis project, which assessed a novel form of acoustic testing to non-invasively detect defects in sweet corn.

### Bugs and such

This program is not yet a polished solution, so there are sure to be some bugs lurking around. Let me know if you find any, through https://github.com/DeanIsMe/Wavepaper_Release. There is a lot of room for improvements and extra features, so please tell me what you would like to see!

Known bugs: 
If you have your display settings set to anything other than 100%, then this program will not be shown correctly.

### Source Code
The source code is not currently released - but I'm not closed off to the idea. This project is hosted on GitHub for ease of distribution.

### License

This work is licensed under the Creative Commons Attribution-NoDerivatives 4.0 International License. To view a copy of this license, visit http://creativecommons.org/licenses/by-nd/4.0/

