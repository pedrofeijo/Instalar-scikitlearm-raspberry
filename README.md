# Instalar-scikitlearm-raspberry
----------------- Instalar conda ---------------

$$ wget http://repo.continuum.io/miniconda/Miniconda3-latest-Linux-armv7l.sh
$$ sudo md5sum Miniconda3-latest-Linux-armv7l.sh # (optional) check md5
$$ sudo /bin/bash Miniconda3-latest-Linux-armv7l.sh # -> change default directory to /home/pi/miniconda3
$$ sudo nano /home/pi/.bashrc # -> add: export PATH="/home/pi/miniconda3/bin:$PATH"
$$ sudo reboot -h now


- Test:
conda
python --version

- If Conda update miss permission of the directory:

$$ sudo chown -R pi miniconda3


Caso ocorra o erro:

	Fetching package metadata: ....
	Solving package specifications: 
	Error: Could not find some dependencies for numpy: blas * openblas

	You can search for this package on anaconda.org with

   		 anaconda search -t conda blas * openblas

execute:

$$ conda install anaconda-client
$$ conda config --add channels rpi
$$ conda install openblas blas



 
------------------ instalar scikit-learn --------------------

$$ conda install scikit-learn

$$ python

	>> import sklearn
	>> import numpy
	>> import scipy


Fim...
