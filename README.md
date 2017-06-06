# Python OpenCV

## Installation:
You need to setup the basic environment to install openCV in your machine. Please follow the instructions for your OS:
 - [Linux](www.pyimagesearch.com/2016/10/24/ubuntu-16-04-how-to-install-opencv/)
 - [Windows](http://docs.opencv.org/3.1.0/d5/de5/tutorial_py_setup_in_windows.html)
 - [OS-X](http://www.pyimagesearch.com/2016/12/19/install-opencv-3-on-macos-with-homebrew-the-easy-way/)

## Basic Concepts:
 - Read Images
```python
import numpy as np
import cv2

# Load an color image in grayscale
# Second argument: cv2.IMREAD_COLOR, cv2.IMREAD_GRAYSCALE, cv2.IMREAD_UNCHANGED
img = cv2.imread('image.jpg',cv2.IMREAD_GRAYSCALE)
```

 - Display Images:
```python
import numpy as np
import cv2
from matplotlib import pyplot as plt

img = cv2.imread('image.jpg',0)
plt.imshow(img, cmap = 'gray', interpolation = 'bicubic')
plt.xticks([]), plt.yticks([])  # to hide tick values on X and Y axis
plt.show()
```
 - Write an Image.
```
cv2.imwrite('gray.png',img)
```
 - Histogram
```python
import cv2
import numpy as np
from matplotlib import pyplot as plt
img = cv2.imread('image.jpg')
color = ('b','g','r')
for i,col in enumerate(color):
    histr = cv2.calcHist([img],[i],None,[256],[0,256])
    plt.plot(histr,color = col)
    plt.xlim([0,256])
plt.show()
```

## Other links:
Here there are other usefull links:
 - [Install on Ubuntu 16.04, Linux Mint](https://www.linuxhint.com/how-to-install-opencv-on-ubuntu/)
 - [Histogram](http://docs.opencv.org/trunk/d1/db7/tutorial_py_histogram_begins.html)
 - [Smoothing Images](http://docs.opencv.org/3.1.0/d4/d13/tutorial_py_filtering.html)
 - [Morphological Transformations](http://docs.opencv.org/3.0-beta/doc/py_tutorials/py_imgproc/py_morphological_ops/py_morphological_ops.html)
