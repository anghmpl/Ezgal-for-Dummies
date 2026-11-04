# EzGal-for-python-3-jupyter #
Disclaimer:  EzGal is a Python program written by Conor Mancone and Anthony Gonzales (2012) for calculating observable parameters (magnitudes, colours, mass-to-light ratios...) for arbitrary stellar population (SPS) models.
(https://iopscience.iop.org/article/10.1086/666502/pdf )
Models include:

 - Bruzual & Charlot 2003 
 - Maraston 2005
 - Charlot & Bruzual 2007
 - Charlot 2009
 - Percival 2009

* **filters** contains the filter transmission functions for all kinds of cameras (e.g. LSST, SDSS, HST....)
* **bc03_ssp_z_0.008_chab.model**  and **bc03_ssp_z_0.02_chab.model** are 2 BC03 models for a single stellar population, with a metallicity of 0.008 and 0.02, respectively. 

The original version runs under Python 2, so several modules have been discontinued and/or renamed libraries and functions, especially the cosmology module. As I am running python 3.14, I have adjusted those to work under python 3.14/ Jupyter, NOT in a python 2 environment.

### Examples ###
* "Inf" = Infinite; important for all integrations is now defined via NumPy, NOT SciPy. Functions have been renamed, e.g.integrate.simps and  integrate.romberg.
* Instead of changing the name at every single instance in the code, I redefined them:
 
```python
import numpy as np
import scipy
from scipy import *
scipy.inf = np.inf
scipy.integrate.simps = scipy.integrate.simpson
scipy.integrate.romberg = scipy.integrate.quad

```


* Link to the original GitHub https://github.com/cmancone/easyGalaxy .

* This repository also includes a folder with filter functions.



## Install ##
If your EzGal survives the next Fedora upgrade, congratulations; otherwise, you might have to reinstall it. I installed it directly in my jupyter environment to make sure there are no problems with the path. 

```python
import sys
!{sys.executable} -m pip uninstall ezgal -y     
!{sys.executable} -m pip install git+https://github.com/cmancone/easyGalaxy.git
```

## Manual ##
The EzGal documentation is not available, so I scanned my version: **EzGal_Documentation.pdf** https://github.com/anghmpl/Ezgal-for-python-3-jupyter/blob/main/EzGal_documentation.pdf

