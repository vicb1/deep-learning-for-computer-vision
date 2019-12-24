# 2_training_the_SSD

Custom object detection can be trained by using the following instructions.  After successfully running this example, your own data can be organized in the same format to create a custom object detection model.

#### To run this implementation:
1. Install the environment based on the `README.md` file from one directory up
1. This training needs an Nvidia GPU, and CUDA installed.  Then, we'll have to ugrade our CPU-only pytorch installation to a GPU installation.  To do this:
   1. For Ubuntu, If you've successfully done the previous steps, nothing extra is required at this step.
   1. For Windows 10 and CUDA 8, run: `conda install -c peterjc123 pytorch cuda80` (or use `cuda80-1.0-h205658b_0.tar.bz2` file in this directory)
   1. For Windows 10 and CUDA 9, run: `conda install -c peterjc123 pytorch cuda90` (or use `cuda90-1.0-h4c72538_0.tar.bz2` file in this directory)
   1. More details [here](https://pytorch.org/get-started/previous-versions/) on previous versions of Pytorch.  Note we need Pytorch version 0.3.1 for this implementation.
1. Download [the training files](https://1drv.ms/u/s!AhJlq_oIk6K6gh0T8YoJITPoZcsw) to the `./data/VOCdevkit/` directory.  Alternatively, the bash scripts under `./data/scripts/` can be run to pull the 2007 and 2012 data from the [PASCAL visual object classes](http://host.robots.ox.ac.uk/pascal/VOC/).

1. Run `train.py`
1. This will take the initialized model file `./weights/vgg16_reducedfc.pth` and build upon it while training.  When complete, this file can then be plugged into the `../1_video_object_detection/` implementation to characterize videos/images
