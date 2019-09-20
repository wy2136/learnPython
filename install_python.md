# Install Miniconda and Python Packages
* Wenchang Yang (wenchang@princeton.edu)
* Department of Geosciences, Princeton University
-----
## Some Concepts

* **Python**: the language and platform.
* **Python packages**: program units for different tasks.
* **conda**: a package that manages packages (can also manage non-Python packages).
* **Anaconda**: a free and open-source distribution of the Python (and R).
    * conda + Python + (1500+) packages.
* **Miniconda**: Minimized version of Anaconda.
    * conda + Python + only a few useful packages.
    * additional packages can be installed later by conda.
* **conda-forge**: the most popular channel where conda gets packages.

## Install Miniconda
> This following instructions focus on macOS. For other operating systems, please read: [Linux](https://conda.io/projects/conda/en/latest/user-guide/install/linux.html#install-linux-silent), [Windows](https://conda.io/projects/conda/en/latest/user-guide/install/windows.html).

1. Download the installer at [this webpage](https://docs.conda.io/en/latest/miniconda.html).
> For macOS select Python version 3.x with name `Miniconda3 MacOSX 64-bit bash`

2. Install. Open the terminal, navigate to where the installer is donwloaded and run the following command:
        bash Miniconda3-latest-MacOSX-x86_64.sh
> Follow the prompts on the installer screens. Accept the defaults if not sure about the settings.

3. Test. Open a new terminal window and run the following command:
        conda list
> A list of installed packages will appear for a successful installation.

## Install Python Packages
After the installation of Miniconda, we already have conda, Python and some limited number of Python packages. But that's not enough for doing research. We still need some core packages popular in geosciences, where `conda` can help us:

        conda install -c conda-forge jupyter numpy scipy matplotlib xarray netCDF4 cartopy
* `conda-forge`: the most popular package channel.
* `jupyter`: provides the nice notebook interface.
* `numpy`: creates the `ndarray`-type data (multidimensional array) and makes it possible for efficient scientific computation in Python.
* `scipy`:`numpy`-based scientific computation tool boxes in different areas (like the Matlab Toolbox).
* `matplotlib`: used for data visualization or making plots.
* `xarray`: adds useful information to the `numpy` array (e.g. name, units, dimension name, coordinates) so that operations on data are more intuitive and user friendly.
* `netCDF4`: used to help `xarray` better read/write netCDF files.
* `cartopy`: used to make base maps.

Of course, it is also possible to install an individual package at each time. For example:

        conda install -c conda-forge bottleneck
        conda install -c conda-forge dask
        conda install -c conda-forge nc-time-axis

## Reference
* https://conda.io/projects/conda/en/latest/user-guide/install/macos.html
* https://medium.com/dunder-data/anaconda-is-bloated-set-up-a-lean-robust-data-science-environment-with-miniconda-and-conda-forge-b48e1ac11646
