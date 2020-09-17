## Fun With Steganography
Just wanted to see if I could detect when an image has been hidden inside another image with 
a process called [steganography](https://towardsdatascience.com/hiding-data-in-an-image-image-steganography-using-python-e491b68b1372).

I used a Python package called ["Stego-LSB"](https://pypi.org/project/stego-lsb/) built by Ryan Gibson.

I found two .png files, and I hid the dice image inside of the grapefruit image.
<p align="center"> <img src=https://github.com/flyboy1378/steganography_detection/images/unaltered.jpg </p>

<p align="center"> <img src=https://github.com/flyboy1378/steganography_detection/images/code.JPG </p>

And we get an output that looks like this (spoiler, you can't see a difference).
<p align="center"> <img src=https://github.com/flyboy1378/steganography_detection/images/steg_closeup.JPG </p>
