# bucketCTF_STEGO CHALLENGES
STEGO CHALLENGES OF BUCKETCTF


**Image-2 -(MISC)::**

https://storage.ebucket.dev/mrxbox98.png

Simple one.
Just strings and then grep through it for bucket.

**strings mrxbox98.png |grep -i 'bucket'**

**FLAG:bucket(m3t4d4t4_4c53f444)**

**Transmission-(MISC)::**

https://storage.ebucket.dev/beamoflight.png

So here I just fired up my linux and started with the basics like strings,binwalk,exiftool ,,etc....

But none yielded any results.

So I went a bit further and tried using LSB,MSB analysis for this using stegsolve.

And voila! you get hidden text from the message.

So just tick through all the planes and get the full data.

Just copy the message to notepad and used Ctrl+F 

**FLAG:bucket{d3c0d3_th3_png_f7c74c1dc7}**

**Drawing-(MISC)::**

https://storage.ebucket.dev/transform.webp

Basically webp images are either png,jpg files which are converted to webp format.

So we need to change it back to that format in order to perform analysis on it.

It can be done by: command :- dwebp transform.webp -o image.png

Now you have the image in png format without any loss of data.

Now that it is a png you can perform the basic analysis using steghide,binwalk,etc..

But none give the output.

Finally if you run zsteg on the png file and grep for 'bucket' you get the required output.

command :zsteg -a image.png | grep -i 'bucket'

**FLAG:bucket{1_l0v3_w3bp_f77c069c7}**
