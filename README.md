## Running MATLAB in Jupyter Notebook
---

*Thanks to Anne Urai and Jiawei Zhuang for prior work on this topic.*

### Installation Prerequisites
- Python 3
- pip
- virtualenv
- MATLAB

### Instructions
1. Create a new folder for your MATLAB notebooks.  For example, `mkdir ~/Documents/matlab_notebooks`.
2. In the new MATLAB notebooks folder, create a virtualenv by running `virtualenv envname`.
3. Activate the virtualenv by running `source envname/bin/activate`.
4. Inside the new virtualenv, install Jupyter with `python3 -m pip install jupyter`.
5. To download and install the MATLAB kernel for Jupyter run:
  - `pip install matlab_kernel`
  - `python -m matlab_kernel install`
6. Check to make sure the kernel was correctly installed by running `jupyter kernelspec list` and looking for the `matlab` kernel.
6. Open your version of MATLAB and type `matlabroot` to get the location of the MATLAB executable.
7. Copy the result of `matlabroot` and then `cd matlabroot/extern/engines/python`. For example, this may be `/Applications/MATLAB_R2018a.app/extern/engines/python`.
8. Setup the Python executables with `python setup.py install`.
9. Return to the MATLAB notebooks folder with `cd path-to-matlab-notebooks-folder`.
9. Open Jupyter by running the command `jupyter notebook`.
10. Once Jupyter Notebook is open, click the New dropdown and `Matlab` should be an option.  Click the `Matlab` option and you will have a new kernel connected to your MATLAB license.
