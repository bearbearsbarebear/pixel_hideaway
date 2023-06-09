# Pixel Hideaway
Pixel Hideaway is a command-line tool for hiding and retrieving secret messages within PNG images. It utilizes the least significant bit (LSB) technique to encode and decode messages, and [LodePNG](https://github.com/lvandeve/lodepng) to interpret the png file.

## Usage
Hiding a message:
>pixel_hideaway.exe image.png -e "This is a secret message."

Retrieving a message:
>pixel_hideaway.exe image.png -d


## Notes
* Each bit of the message is hidden within the least significant bit of the color channels of the image.
* The image file should be in the PNG format.
* The message should be enclosed in double quotes ("<message>") when using the encode mode.
* Ensure that the message does not exceed the available capacity within the image.
* The decode mode decodes the whole image, so you might also get garbage information.
