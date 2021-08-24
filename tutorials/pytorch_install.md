# What to know in installing PyTorch

## (1) Using `conda` is recommended to manage PyTorch environments. 

Conda is a mix of package manager as well as environment manager. Particularly installing **Miniconda** is recommended.  

![Conda vs Miniconda vs Anaconda](https://linuxnetmag.com/wp-content/uploads/2020/11/MinicondavsAnaconda.jpg)

Go to [this link](https://docs.conda.io/en/latest/miniconda.html), and install one for your PC.  

## (2) You can also use `pip` when using `conda` has some troubles. 

My PC was struggled to install PyTorch (particularly GPU version) in using `conda`. 
```
conda install pytorch torchvision torchaudio cudatoolkit=11.1 -c pytorch-lts -c conda-forge
```
The process by the above command seemed to be somehow halt (or maybe its download speed was very slow) in the middle of installing `pytorch`. Thus, I forcefully aborted the process, and instead used `pip` for the installation. 
```
pip3 install torch==1.8.2+cu111 torchvision==0.9.2+cu111 torchaudio===0.8.2 -f https://download.pytorch.org/whl/lts/1.8/torch_lts.html
```

The above install commands can be seen in this [link](https://pytorch.org/get-started/locally/#windows-installation).


Even if some packages were installed by `pip`, they also can be seen by `conda list`. 








