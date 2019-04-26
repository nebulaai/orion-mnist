# Orion sample AI task - single GPU - DCGAN #


# Introduction #

This is a sample AI script for testing task-processing pipeline on Nebula AI Orion working node.

# Model Description #

A sample code using Deep Convolutional Generative Adverserial Networks, to generate handwritten digital images.
We use the MNIST dataset to train the generator and discriminator for GAN. The generator generates handwritten digital images and will save to result folder.

# Results #

Results of this model include:

- Checkpoints for tensorboard visualization, saved in _/mnist/checkpoints_ folder. 
- The generator will produce one image per epoch, and pool all saved images as a GIF. Images and GIF will be saved in _mnist/result_ folder. 


# Remarks # 

- Nebula AI working node will execute the file "DCGAN_Demon.py", and save all results in the directory _mnist_.
- The entire task-processing time on Orion platform takes around 20 minutes.
- Users will be able to retrieve contents from result directory, together with system execution log.
- For more details on how-to-guides for task submission, please refer to instructions on Nebula AI developer portal. 

#Execution log from Orion #

> 2018-10-05 18:22:42-INFO- Miner starts processing this task (0x8861c3f8158779d26b61f6FaD997376FbFD9aBA8)
> 2018-10-05 18:22:42-INFO- starting to download task script
> 2018-10-05 18:22:44-INFO-  task script downloaded
> 2018-10-05 18:22:44-INFO- starting to install packages from requirements.txt
> 2018-10-05 18:22:57-INFO-  packages downloaded 
> 2018-10-05 18:22:57-INFO- starting to execute script
> 2018-10-05 18:41:38-INFO- ========Script is executed======
> 2018-10-05 18:41:38-INFO- The results is uploaded.