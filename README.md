# EzGal-for-python-3-jupyter #
Disclaimer:  EzGal is a Python program written by Conor Mancone and Anthony Gonzales (2012) for calculating observable parameters (magnitudes, colours, mass-to-light ratios...) for arbitrary stellar population (SPS) models.
(https://iopscience.iop.org/article/10.1086/666502/pdf )


* The original version runs under Python 2, so several modules have discontinued and/or renamed libraries and functions, especially the cosmology module.
* As I am running python 3.14, I have adjusted those to work under python 3.14/ Jupyter, NOT in a python 2 environment.

### Examples ###
* Indefinit is now defined via numpy, NOT scipy, and fuctions for integration have been renamed, e.g.integrate.simps and  integrate.romberg.
* Instead of changing the name at every single instance in the code, I redefined them:
 
```python  
import scipy
from scipy import *
scipy.inf = np.inf
scipy.integrate.simps = scipy.integrate.simpson
scipy.integrate.romberg = scipy.integrate.quad

```


* Here is the link to the original GitHub https://github.com/cmancone/easyGalaxy .

* This repository also includes a folder with filter functions.

* The original webpage which provided the models (e.g. Bruzual & Charlot 2003, Maraston 2005...) does not exist anymore, so I added a few models to this repository ( bc03_ssp_*.model ) which you can use to run the program.


## Install ##
If your EzGal survies the next Fedora upgrade, congratulations; otherwise, you might have to reinstall it. I installed it directly in my jupyter environment to make sure there are no problems with the path. 

```python
import sys
!{sys.executable} -m pip uninstall ezgal -y
!{sys.executable} -m pip install git+https://github.com/cmancone/easyGalaxy.git
```

## Manual ##
The EzGal documentation is not available, so I scanned my version: **EzGal_Documentation.pdf** https://github.com/anghmpl/Ezgal-for-python-3-jupyter/blob/main/EzGal_documentation.pdf

