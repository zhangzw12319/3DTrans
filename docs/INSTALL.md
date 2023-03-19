# Installation

### Requirements
All the codes are tested in the following environment:
* Linux (tested on Ubuntu 16.04)
* Python 3.6+
* PyTorch 1.7.0, PyTorch 1.8.0, PyTorch 1.8.1
* CUDA 11.1
* [`spconv v2.x`](https://github.com/traveller59/spconv)
* gcc version >= 5.4.0


### Install 3DTrans
NOTE: Please re-install `3DTrans` by running `python setup.py develop` even if you have already installed previous version.

a. Clone this repository.
```shell
git clone https://github.com/PJLab-ADG/3DTrans.git
```

b. Install the dependent libraries as follows:

* Install the python dependent libraries.
  ```shell
    pip install -r requirements.txt 
  ```

* Install the gcc library, we use the gcc-5.4 version

* Install the SparseConv library, we use the implementation from [`[spconv]`](https://github.com/traveller59/spconv). 
    * It is recommended that you should install the latest `spconv v2.x` with pip, see the official documents of [spconv](https://github.com/traveller59/spconv).
    * Also, you should choice **the right version of spconv**, according to **your CUDA version**. For example, for CUDA 11.1, pip install spconv-cu111
  
c. Install this `pcdet` library and its dependent libraries by running the following command:
* NOTE: If you install this repository on the S-Project, please use **srun** to submit the installation command as follows:
```shell
srun -p shlab_adg -N 1 -c 10 python setup.py develop
```

* Normal installation
```shell
python setup.py develop
```