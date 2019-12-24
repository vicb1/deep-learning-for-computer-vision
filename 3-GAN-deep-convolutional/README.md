# Deep Convolutional Generative Adversarial Network (DCGAN) algorithm

Implementation of a DCGAN algorithm per the following methodology:
- [Unsupervised Rrepresentation Learning With Deep Convolutional Generative Adversarial Networks](https://arxiv.org/pdf/1511.06434.pdf)

This uses the [CIFAR-10 dataset](http://www.cs.toronto.edu/~kriz/cifar.html) for training.

For example we take image examples such as these:

![image](https://github.com/vicb1/deep-learning-for-computer-vision/blob/master/3-GAN-deep-convolutional/results/real_samples.png?raw=true)


And through the DCGAN algorithm, we can iteratively generate fake images such as the ones below:

![image](https://github.com/vicb1/deep-learning-for-computer-vision/blob/master/3_Deep_Convolutional_GAN/results/fake_samples_epoch_024.png?raw=true)

#### To set up environment on Ubuntu 18.04:
1. Download this repository, then run the following commands in the command prompt to create this environment:
   1. `cd <your_path>/3_SSD_object_detection/`
   1. `conda env create -f compVisEnv_Ubuntu18.yml`
1. Note this can then be exported/backed up by running the following, if desired:
   1. `source activate compVisEnv_Ubuntu18`
   1. `conda env export > environment.yml`

#### To set up environment on Windows 10:
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
   1. `conda install -c peterjc123 pytorch-cpu` (the latest `pytorch` package won't work with this implementation. Also if this package is no longer active, the file `./windows_install/pytorch-cpu-0.3.1-py36_cpuhe774522_2.tar.bz2` in this directory can be installed through conda instead)
   1. `pip install torchvision`
   
#### To run the CPU version (~10x slower than CUDA version)
1. Run file `./dcgan_CPU.py`

#### To run the CUDA GPU version on Ubuntu 18.04
1. Ensure proper CUDA installation
1. Run file `./dcgan_CPU.py`

#### To run the CUDA GPU version on Windows 10
1. In addition to the instructions above, do the following.
1. For Windows 10 and CUDA 8, run: `conda install -c peterjc123 pytorch cuda80` (or use `./windows_install/cuda80-1.0-h205658b_0.tar.bz2` file in this repository)
1. For Windows 10 and CUDA 9, run: `conda install -c peterjc123 pytorch cuda90` (or use `./windows_install/cuda90-1.0-h4c72538_0.tar.bz2` file in this repository)
   1. More details [here](https://pytorch.org/get-started/previous-versions/) on previous versions of Pytorch.  Note we need Pytorch version 0.3.1 for this implementation.
1. Ensure proper CUDA installation
1. Run file `./dcgan_CPU.py`
