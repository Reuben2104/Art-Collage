# Art-Collage

**Overview**
The goal of this assignment is to perform several operations on digital images.
Your cellphone are computers with lenses and light-sensitive devices capable of capturing images in digital form, and your computer has photo-editing software that allows you to process those images. You can crop them, enlarge and reduce them, adjust the contrast, brighten or darken them, remove redeye, and a myriad of other operations. Many such operations are easy to implement, given a simple data type that captures the idea of a digital image.


**Methods implemented by me:**

Collage keeps at all times two digital images as Pictures:
  - original picture, which is the image from the input file without modification. 
  - collage picture, which is the image you will perform operations on.
      - The image has collageDimension x collageDimension tiles.
      - Each tile is made of tileDimension x tileDimension pixels.

**One-Argument Constructor**
  - set default values of collage dimension to 4 and tile dimension to 150.
  - initializes original picture with the filename image.
  - initializes collage picture as a Picture of tileDimension*collageDimension x tileDimension*collageDimension where each pixel is black.
  - update collagePicture to be a scaled version of original.


**Three-Arguments Constructor**
  - set default values of collage dimension and tile dimension to argument values.
  - initializes original picture with the filename image.
  - initializes collage picture as a Picture of tileDimension*collageDimension x tileDimension*collageDimension, where each pixel is black.
  - update collage picture to be a scaled version of original picture.

**Scale**
  - used in both constructors.
  - changes the size of a picture to fit into another.

**makeCollage**
  - make a tile  of tileDimension x tileDimension pixels by scaling down the original picture.
  - update the collage picture to be a collage of these tiles. Meaning, each tile is repeated in the image.
  - the collage picture will have collageDimension x collageDimension tiles.

**replaceTile**
  - replaces a tile on the collage picture with another image.

**colorizeTile**
  - colorizes a tile in the collage picture using red, green, or blue component.
  - to colorize a tile “green” do for every pixel:
      - get the pixel’s color’s green intensity.
      - update/set the pixel with only it’s green component.
      - Color color = picture.get(col, row);
        int g = color.getGreen();
        color.set(col, row, new Color(0, g, 0));

**grayscaleTile**
  - grayscale a tile of the collage picture.
  - update the pixel’s color of a tile to have the grayscale value computed by applying the toGray() method provide.
