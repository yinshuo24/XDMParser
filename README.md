# ParseDepthFile
##Introduction
load and parse XDM format depth file.<br>
It read the reference image and depth image embedded in the depth file and draw them on the screen.
It also reads other attributes of depth file and print them out.<br>
For more information on XDM specification, you can refer to https://software.intel.com/en-us/articles/the-extensible-device-metadata-xdm-specification-version-10<br />
Here I use `material-ui` to beautify the interface. For more information about `material-ui`, please refer 
to their website http://www.material-ui.com/#/<br />
###Installation
1. Install material-ui following http://www.material-ui.com/#/get-started/installation<br />
2. Install browserify: `npm install -g browserify`<br />
3. Install jsx support: `npm install --save babelify babel-preset-react`
4. build bundle: `browserify -t [ babelify --presets [ react ] ] main.js -o bundle.js`

##Usage
open `http://localhost/path-to-index.html` in google chrome. it doesn't work in firefox.<br>
Because I use TypedArray.prototype.slice whcih is not support in firefox, at least in my firefox.
##Acknowledge
I used and modified three js libraries written by others.<br>
depth-reader.js: I use it to parse depth file. From https://github.com/DavisReef/depth-reader-js<br>
png.js: I use it to decode png image. From https://github.com/arian/pngjs<br>
decoder.js: I use it to decode jpeg image. From https://github.com/eugeneware/jpeg-js<br>
###Status
Have problem display html marks		--fixed 2015/12/14<br />
Can't Parse xdm written by sdk R5	--fixed 2015/12/16<br />
