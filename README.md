# Introduction
Throughout this project, morphological operations were being used to Process Microscopic Blood Smear Images and Differentiate Erythrocytes from Other Blood Cells.

# Requirement
* Matlab > R2019b
* Matlab Live Editor

## Dataset
Download Dataset ALL_IDB1 from [Here](https://homes.di.unimi.it/scotti/all/)

# Implementation
First, the RGB coloring transformed to HSV (hue, saturation, value) coloring for further considerations. The code below was responsible for that:
```Matlab
hsvI = rgb2hsv(a)
```
Results are showed bellow:
![Original Image](https://github.com/pmadinei/MO-cnt-blood/blob/master/Results/Original%20Image.png)
![HSV Transformed](https://github.com/pmadinei/MO-cnt-blood/blob/master/Results/HSV%20Transformed.png)

Then, for Morphological operations, "Dilation & Erosion" plus "Open & Close" were implemented; Thus, as the final level, the holes were being filled with the code bellow:
```Matlab
red = imfill(red,'holes');
```
As it's been shown bellow, the red blood cells are clearly visible and countable. Consequently, a simple CNN can count it pretty easily.
![Filled Holes](https://github.com/pmadinei/MO-cnt-blood/blob/master/Results/Filled%20Holes.png)

# Reference
* [A novel approach for segmentation and counting of overlapped leukocytes in microscopic blood images](https://www.sciencedirect.com/science/article/abs/pii/S0208521620300267#fn0010)
* [An Automated Method for Counting Red Blood Cells using Image Processing](https://www.sciencedirect.com/science/article/pii/S1877050920308747)
