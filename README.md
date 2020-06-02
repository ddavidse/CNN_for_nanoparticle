# CNN_for_nanoparticle
This repository contains Convolutional Neural Network code used for the paper "Convolutional Neural Network Applied for Nanoparticle Classification using Coherent Scaterometry Data". 

Authors: D. KOLENOV*, D. DAVIDSE , J. LE CAM , AND S.F. PEREIRA

*Corresponding author: d.kolenov@tudelft.nl

----------------------------------------------------------------------------------------------------------------------------------

MAIN CODE GUIDE:

1. Download the code files CNN_functions.py and CNN_masterscript.py and put them in the same folder
2. Download the datasets from https://doi.org/10.4121/uuid:516ab2fa-4c47-42f8-b614-5e283889b218
3. Open CNN_masterscript.py
2. On lines 46 and 49 (and optionally also 52) enter the correct paths
3. Use lines 56-98 to set the desired parameters and features
4. In case of no CUDA: use ctrl+F to go through the script and comment out all lines that contain "cuda"
5. Run the script

For a basic test, make confusion_flag = True and batchnorm_flag = True while leaving the rest as False

----------------------------------------------------------------------------------------------------------------------------------

PCA - trajectory.py is a seperate version of CNN_masterscript that was used for plotting trajectories on loss contour plots that were obtained with PCA

----------------------------------------------------------------------------------------------------------------------------------

EXAMPLE GUIDE:

To use the example code:

1. Download the code files example.py and CNN_functions.py and put them in the same folder
2. Download the saved weights file "initial_weights_for_example.pth"
3. Download the datasets  from https://doi.org/10.4121/uuid:516ab2fa-4c47-42f8-b614-5e283889b218
4. Open example.py
5. On line 46, enter the desired folder to store outputs
6. On line 49, enter the location of "main dataset - 100x 100"
7. On line 52, enter the location of "elephants - 100x 100"
8. On line 62, enter the location of "initial_weights_for_example.pth"
9. Run the script

----------------------------------------------------------------------------------------------------------------------------------

REPRODUCIBILITY

This is only possible when working on the CPU and setting a random seed. This is done in example.py, which is why the training curve looks the same every time. When using a GPU via CUDA, there is inherent randomness that, to our knowledge, cannot be prevented from inside a python script. For more information, see https://pytorch.org/docs/stable/notes/randomness.html#pytorch

----------------------------------------------------------------------------------------------------------------------------------

OPENMAX GUIDE:

1. Download CNN_functions.py, OpenMax_masterscript.py, compute_openmax.py and evt_fitting.py from the folder OpenMax_code and put them in the same folder
2. On line 44, enter the directory where outputs should be stored
3. On line 47, enter the directory of the main dataset used for training
4. On line 50, enter the directory of the fooling dataset
5. Run the script
