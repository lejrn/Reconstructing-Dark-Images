(Not completed yet)

# Reconstructing-Dark-Images
This github repository displays the entire process of building up this project, in which the goal is to restore lost data in dark images into bright fully-detailed images with neural networks.

# Why use Machine Learning? 
## (more precisely: use CNNs)
Given dark images, 

# Performance
How could we measure the performance? What metrics could be the best to use?
So far, the answers are PSNR (Peak signal-to-noise ratio) and SSIM (Structural Similarity) metrics.

I have used pre-defined `python`

# Methodology
1.

# Goals
1. Gathering knowlodge about Deep learning, especially Residual Networks and Unet Networks
2. Programming a neureal network that is trained with dark photos and its pair
3. Optimizing its specifications, as in batch-size, depth of layers, input files sizes, learning rates, and so on
4. Using SID dataset by <insert credits here> and examine our performance to theirs

# Architecture
![Alt text](./SVGs/Architecture__.svg)

# class TensorRawImage + class RAWImage
## First off, what is the difference between JPG and RAW formats?
JPG format has a depth bit of 8bits for every channel (R,G,B), meaning: every pixel gets values in between 0 up to 255.
> 2^8=255
  
RAW format has a depth bit of 16bits for every channel (R,G,B[,G]), meaning: every pixel gets values in between 0 up to... 65536!
> 2^16=65536

Therefore, a RAW image file would normally have a larger range of value for every pixel, which can help the model training become more precise, when switching from JPG to RAW.
> Note: in practice, every DSLR stors RAW files and postprocesses these files into other formats. For instance, it crops and compresses the JPG image out of the RAW file.

## Problem: PIL doesn't support RAW files
  
In order to improve the training process, I figured out that using RAW files would yield in more details. Problem was that fastai has been based on `PIL` for handling image files, which doesn't support RAW files. Therefore, I needed to create new classes that inherit feautres from `rawpy` library, that support RAW files.
  
## Creating new classes
![Alt text](./SVGs/TensorRawImage__.svg)
  
