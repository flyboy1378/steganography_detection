## Fun With Steganography
Just wanted to see if I could detect when an image has been hidden inside another image with 
a process called [steganography](https://towardsdatascience.com/hiding-data-in-an-image-image-steganography-using-python-e491b68b1372).
I used a Python package called ["Stego-LSB"](https://pypi.org/project/stego-lsb/) built by Ryan Gibson.

I found two .png files, and I hid the dice image inside of the grapefruit image.
<p align="center"> <img src=https://github.com/flyboy1378/steganography_detection/blob/master/images/unaltered.JPG </p>

<p align="center"> <img src=https://github.com/flyboy1378/steganography_detection/blob/master/images/code.JPG </p>

And we get an output that looks like this (spoiler, you can't see a difference).
<p align="center"> <img src=https://github.com/flyboy1378/steganography_detection/blob/master/images/steg_closeup.JPG </p>

I was curious if I could see a difference between a RGBA histogram for each the steg.png and the original grapefruit.png. 
Its minute, but there is a difference!
<p align="center"> <img src=https://github.com/flyboy1378/steganography_detection/blob/master/images/histo_compare.png </p>

I figured if I create a numpy array out both the steg.png and the original grapefruit.png, do an array subtract
`img_diff = np.subtract(gf_np, steg_np)`, then a `imshow(img_diff)` we can actually see where the dice.png was hidden.
<p align="center"> <img src=https://github.com/flyboy1378/steganography_detection/blob/master/images/np_diff.JPG </p>

Just to show that the dice image could be recovered, I reversed the stego-LSB process from above.
<p align="center"> <img src=https://github.com/flyboy1378/steganography_detection/blob/master/images/recovery_code.JPG </p>
<p align="center"> <img src=https://github.com/flyboy1378/steganography_detection/blob/master/images/recovery.JPG </p>
