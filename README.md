(Not completed yet)

# Reconstructing-Dark-Images
This github repository displays the entire process of building up this project, in which the goal is to restore lost data in dark images into bright fully-detailed images with neural networks.

# Why use Machine Learning? (Or more precisely: Convolutional Neural Networks)
Using 

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

# TensorRawImage
In order to improve the training process, I figured out that using RAW files would yield in more details. That's why I needed to adjust the code to supprot RAW files, since PIL library doesn't support RAW files. Problem was that fastai has been based on PIL for handling image files.

![Alt text](./SVGs/TensorRawImage__.svg)
  
