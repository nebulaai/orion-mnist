# Orion sample AI task - single GPU - DCGAN #


# Introduction #

This is a sample AI script for testing task-processing pipeline on Nebula AI Orion working node.

# Model Description #

A sample code using Deep Convolutional Generative Adverserial Networks, to generate handwritten digital images.
We use the MNIST dataset to train the generator and discriminator for GAN. The generator generates handwritten digital images and will save to result folder.

# How to run AI model on Orion
- Step one: Packup your AI model into a zip by [Orion-Script-Converter](https://github.com/nebulaai/orion-script-converter).
    
    This convertor will analyze the python code (.py) or jupyter notebook (.ipynb) and ask you a few questions to configure the task. 
    After install the Orion-Script-Converter, start the convertor by typing command "convert2or".
    **Note:**
    - Enter your project
    - Type command 'convert2or'
    
        Input parameters according to the prompt:
        
        1.(Required) Project path: 
	    (Press 'Enter' or '.' for the current directory, '..' for the parent directory of the current folder): 
        
        Input the Python3 project path, either relative path or absolute path. 
        'Enter' or '.' represents the current folder(default) and the '..' means the parent folder 
        of the current path.
        
        2.(Required) entry-point file path(executable file path):
        
        Input the name of entry-point file. This path should inside the Project path.
        
        3.Data configuration: 
	        Do you have external data(data stored outside your project database)
	        that needs to be downloaded from a specific uri (y/n)?
	        
        Set data configuration. If 'y', the following two inputs prompt. Otherwise, this step will skip.
        
            External data uri:  
            
            Input the data uri to get your external data
            
            Path to save the downloaded data within your project:
            
            Input the path(inside your project) to save your downloaded external data.  
            
        4.Path for the task results(project output directory):
        
            Your project output directory holds your output files. 
            If you have such a directory in your project, input it here. 
            Otherwise, there will be no output files.
            
        5.A NBAI task will be created and saved in the 'task_files' folder 
           which is a sibling folder of your project. 

-Step two: submit your AI zip file to Orion. Please follow [this procedure](https://www.youtube.com/watch?v=FzFNgC4sL3g)

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