# Cartoonify-Image-python

Imread is a method in cv2 which is used to store images in the form of numbers. This helps us to perform operations according to our needs. 
The image is read as a numpy array, in which cell values depict R, G, and B values of a pixel.

To convert an image to a cartoon, multiple transformations are done. Firstly, an image is converted to a Grayscale image. Yes, similar to the old day’s pictures.! Then, the Grayscale image is smoothened, and we try to extract the edges in the image. 
Finally, we form a color image and mask it with edges. This creates a beautiful cartoon image with edges and lightened color of the original image.
