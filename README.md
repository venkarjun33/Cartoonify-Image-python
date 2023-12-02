# Cartoonify-Image-python

Imread is a method in cv2 which is used to store images in the form of numbers. This helps us to perform operations according to our needs. 
The image is read as a numpy array, in which cell values depict R, G, and B values of a pixel.

To convert an image to a cartoon, multiple transformations are done. Firstly, an image is converted to a Grayscale image. Yes, similar to the old day’s pictures.! Then, the Grayscale image is smoothened, and we try to extract the edges in the image. 
Finally, we form a color image and mask it with edges. This creates a beautiful cartoon image with edges and lightened color of the original image.

cvtColor is a method in cv2 which is used to transform an image into the colour-space. Here, our first step is to convert the image into grayscale. Thus, we use the BGR2GRAY flag. This returns the image in grayscale.

After each transformation, we resize the resultant image using the resize() method in cv2 and display it using imshow() method. This is done to get more clear insights into every single transformation step.

To smoothen an image, we simply apply a blur effect. This is done using medianBlur() function. Here, the center pixel is assigned a mean value of all the pixels which fall under the kernel. In turn, creating a blur effect.

Cartoon effect has two specialties:
-Highlighted Edges
-Smooth colors

To retrieve the edges and highlight this is attained by the adaptive thresholding technique. The threshold value is the mean of the neighborhood pixel values area minus the constant C. C is a constant that is subtracted from the mean or weighted sum of the neighborhood pixels. Thresh_binary is the type of threshold applied, and the remaining parameters determine the block size.

Then we prepare a lightened color image that we mask with edges at the end to produce a cartoon image. We use bilateralFilter which removes the noise. It can be taken as smoothening of an image to an extent.

So, let’s combine the two specialties. This will be done using MASKING. We perform bitwise and on two images to mask them.
This finally CARTOONIFY our image!
