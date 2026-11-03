# Ezgal-for-python-3-jupyter
Disclaimer:  EzGal is a Python program written by Conor Mancone and Anthony Gonzales (2012) for calculating observable parameters (magnitudes, colours, mass-to-light ratios...) for arbitrary stellar population (SPS) models.
(https://iopscience.iop.org/article/10.1086/666502/pdf )


* The original version runs under Python 2, so several modules have discontinued libraries and functions, especially the cosmology module.
* As I am running python 3.14, I have adjusted those to work under python 3.14/ Jupyter, NOT in a python 2 environment.
* Here is the link to the original GitHub https://github.com/cmancone/easyGalaxy .

* This repository also includes a folder with filter functions.

* The original webpage which provided the included models (e.g. Bruzual & Charlot 2003, Maraston 2005...) does not exist anymore, so I added a few models to this repository(bc03_ssp_*.model) which you can use to run the program.


**Install**
I installed it directly in my jupyter environment, to make sure there is no problems with the set path to the executables. 


import sys
!{sys.executable} -m pip uninstall ezgal -y
!{sys.executable} -m pip install git+https://github.com/cmancone/easyGalaxy.git
