# pixels

This repository is a placeholder for testing image data conversions

## NOTICE

A potential **rewrite** may happen, and some information below can be outdated!

## How To

### Process 1: Pixel Extraction

Before running the engine, you must **convert/extract** your image
into a **pixel data set**. (Can be either RGB or RGBA data.)

**BUT before you extract data**, you must **shrink** your image
by an [image resizer](https://imageresizer.com).

(It is necessary to not crash your computer, trust me.)

* Head to an image resizer website (Example: https://imageresizer.com)
* Select your image and shrink your image by **percentage**
	* Your image must be either between **100,000-250,000** pixels (depending on your performance)
		* Simply multiply the *width* by the *height* to get the amount of pixels
		* You can resize it to any dimensions, but the *above* range is recommended
* Simply download the resized image and move onto the steps below

Extracting pixel data from an image:

* Go to the [Pixel Values Extractor](https://www.boxentriq.com/code-breaking/pixel-values-extractor)
* Select your *resized* image and select `RGB` or `RGBA` from **Mode**
* Click on `Extract` and copy the outputted data below the button
* Paste the data into a file (Github file, or Pastebin file)
* Publish it and copy the **raw** file path

### Process 2: Image Drawing

* Open `Constants` in `ImageRGB` module to change settings
	* Change the `ReposUrl` to change the main repository url
		* The image path must be from a **raw** path
	* Change the `PathFile` to set the target file directory relative to the `ReposUrl`
	* To draw multiple images, set `MultiMediaMode` in settings to `true`
		* Change the `MultiMediaConfig` table to a set of file paths for the images
	* To reduce lag from drawings, set `UnionizePixels` to `true`
	* To draw pictures from **RGBA** data, set `RGBAMode` to `true`
		* Change `UnionMethod` to `1` or `2` to use different union methods
		* `1` - `SameColorGroups` will unionize pixels with the same color (takes less time; depending on the amount of color groups)
		* `2` - `PixelSections` will unionize sections of the image (reduces more lag)
	* To use the built-in *Freecam*, set `BirdEyeMode` to `true`
		* You can set the settings in `BirdEyeValues`
* Run the game and activate with the prompt on the green block
	* The engine will then start drawing images by your image data!
