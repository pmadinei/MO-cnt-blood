# Introduction
Throughout this project, morphological operations were being used to count Red and White cells in microscopic blood smear images. 

# Implementation
First, the RGB coloring transformed to HSV (hue, saturation, value) coloring for further considerations. The code below was responsible for that:
```Matlab
hsvI = rgb2hsv(a)
```
Results Is showed bellow:

Then, for Morphological operations, "Dilation & Erosion" plus "Open & Close" were implemented; Thus, as the final level, the holes were being filled with the code bellow:
```Matlab
red = imfill(red,'holes');
```
