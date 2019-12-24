# Single Shot MultiBox Detector (SSD) algorithm

Examples of the [SSD algorithm](https://arxiv.org/pdf/1512.02325.pdf), where we input labeled training images, create a training file, then use this training file to quickly detect labels of new images.  This implementation converts an input video into a labeled output video, which can exhibit the speed of this object detection.

This uses [this pytorch SSD implementation](https://github.com/amdegroot/ssd.pytorch) as a base.

See the following image from the original paper exhibiting the wide variety of objects able to be detected, as well as being able to detect multiple possibly closely overlapping objects at once:

![image](https://github.com/vicb1/deep-learning-for-computer-vision/blob/master/2_SSD_object_detection/ssd_examples.png?raw=true)

#### To get these examples running on Ubuntu 18.04:
1. Download this repository, then run the following commands in the command prompt to create this environment:
   1. `cd <your_path>/3_SSD_object_detection/`
   1. `conda env create -f compVisEnv_Ubuntu18.yml`
1. Note this can then be exported/backed up by running the following, if desired:
   1. `source activate compVisEnv_Ubuntu18`
   1. `conda env export > environment.yml`

#### To get these examples running on Windows 10:
1. Download this repository, then run the following commands in the command prompt to create this environment:
   1. `cd <your_path>\3_SSD_object_detection\`
   1. `conda env create -f compVisEnv_Windows10.yml`
1. Note this can then be exported/backed up by running the following, if desired:
   1. `activate compVisEnv_Windows10`
   1. `conda env export > environment.yml`

#### If issues are experienced with the approach above, you can install the environment step by step to help troubleshoot, with the following instructions:
1. Create a new Conda environment for Python 3.6, named `compVisEnv`
1. Run the following commands in the command prompt
   1. `activate compVisEnv`
   1. `pip install opencv`
   1. `pip install imageio`
   1. `conda install ffmpeg -c conda-forge`
   1. `conda install -c peterjc123 pytorch-cpu` (the latest `pytorch` package won't work with this implementation. Also if this package is no longer active, the file `pytorch-cpu-0.3.1-py36_cpuhe774522_2.tar.bz2` in this directory can be installed through conda instead)
   1. `pip install torchvision`
