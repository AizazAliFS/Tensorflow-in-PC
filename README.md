
#Tensorflow Installation Guidance For PC

#Manual Python Setup
•	Instructor: Aizaz Ali, Youtube Channel:  FutureScope
•	For more information visit youtube channel: https://www.youtube.com/c/FutureScope/.

#Software Installation
This class is technically oriented. A successful student needs to be able to compile and execute Python code that makes use of TensorFlow for deep learning. There are two options for you to accomplish this:
•	Install Python, TensorFlow and some IDE (Jupyter, TensorFlow, and others)
•	Use Google CoLab in the cloud

#Installing Python and TensorFlow
First step is download python and install it but I prefer download Anaconda or Miniconda. Miniconda is the minimal set of features from the extensive Anaconda.
I prefer to download Anacodna from the official link here.. 
URL: https://repo.anaconda.com/archive/Anaconda3-2021.05-Windows-x86_64.exe or https://www.anaconda.com/products/individual

After installation of Anaconad python will automatically be installed in your computer or laptop. You must make sure that TensorFlow has the version of Python that it is compatible with. The best way to accomplish this is with an Anaconda environment. Each environment that you create can have its own Python version, drivers, and Python libraries. I suggest that you create an environment to hold the Python instance for this class. Use the following command to create your environment. I am calling the environment tensorflow, you can name yours whatever you like
.
conda create –n tf tensorflow 
To enter this environment, you must use the following command:
conda activate tensorflow
We will now install TensorFlow. We will make use of conda for this installation. 

How to install TensorFlow for either a CPU or GPU. To use GPU, you must have a compatible NVIDIA GPU.

#Install TensorFlow for CPU Only
The following command installs TensorFlow for CPU support. Even if you have a GPU, it will not be used.
conda install -c anaconda tensorflow

#Install TensorFlow for GPU and CPU
The following command installs TensorFlow for GPU support. All of the complex driver installations should be handled by this command.
conda install -c anaconda tensorflow-gpu

#Install Additional Libraries for ML
There are several additional libraries that you will need for this course. This command will install them. Make sure you are still in your tensorflow environment.
conda env update --file tools.yml

The tools.yml file is located in the root directory for this GitHub repository.

#Register your Environment
The following command registers your tensorflow environment. Again, make sure you "conda activate" your new tensorflow environment.

python -m ipykernel install --user --name tensorflow --display-name "Python 3.8 (tensorflow)"

#Testing your Environment
You can now start Jupyter notebook. Use the following command.
jupyter notebook
You can now run the following code to check that you have the versions expected.

# What version of Python do you have?
import sys

import tensorflow.keras
import pandas as pd
import sklearn as sk
import tensorflow as tf

print(f"Tensor Flow Version: {tf.__version__}")
print(f"Keras Version: {tensorflow.keras.__version__}")
print()
print(f"Python {sys.version}")
print(f"Pandas {pd.__version__}")
print(f"Scikit-Learn {sk.__version__}")
gpu = len(tf.config.list_physical_devices('GPU'))>0
print("GPU is", "available" if gpu else "NOT AVAILABLE")

Tensor Flow Version: 2.1.0
Keras Version: 2.2.4-tf

Python 3.7.7 (default, May  6 2020, 11:45:54) [MSC v.1916 64 bit (AMD64)]
Pandas 1.0.5
Scikit-Learn 0.23.1
GPU Not  available
