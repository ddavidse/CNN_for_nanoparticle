# ConvNet
This repository contains Convolutional Neural Network code used for the paper "Convolutional Neural Network Applied for Nanoparticle Classification using Coherent Scaterometry Data". 

Authors: D. KOLENOV*, D. DAVIDSE , J. LE CAM , AND S.F. PEREIRA

*Corresponding author: d.kolenov@tudelft.nl

----------------------------------------------------------------------------------------------------------------------------------

To use the code:

1. Download the code files CNN_functions.py and CNN_masterscript.py and put them in the same folder
2. Download the datasets here (insert url later)
3. Open CNN_masterscript.py
2. On lines 46 and 49 (and optionally also 52) enter the correct paths
3. Use lines 56-98 to set the desired parameters and features
4. In case of no CUDA: use ctrl F to go through the script and comment out all cuda lines
5. Run the script

For a basic test, make confusion_flag = True and batchnorm_flag = True while leaving the rest as False

----------------------------------------------------------------------------------------------------------------------------------

PCA - trajectory.py is a seperate version of CNN_masterscript that was used for plotting trajectories on loss contour plots that were obtained with PCA

----------------------------------------------------------------------------------------------------------------------------------

REPRODUCIBILITY

This is only possible when working on the CPU and setting a random seed. When using a GPU via CUDA, there is inherent randomness that, to our knowledge, cannot be prevented from inside a python script. For more information, see https://pytorch.org/docs/stable/notes/randomness.html#pytorch
