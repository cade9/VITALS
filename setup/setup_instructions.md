# Repository Setup Instructions

> **This repository uses a Python environment similar to the [EMIT Data Resources Repository](https://github.com/nasa/EMIT-Data-Resources), with the addition of the `scikit-image` library. If you have previously installed the `emit_tutorials` environment, you can simply add this library and use that environment. If you plan to work with the EMIT-Data-Resources Repository, this `lpdaac_vitals` environment can be used.**

The how-tos and tutorials in this repository require a [NASA Earthdata account](https://urs.earthdata.nasa.gov/), an installation of [Git](https://git-scm.com/downloads), and a compatible Python Environment. We recommend [mamba](https://mamba.readthedocs.io/en/latest/) to manage Python packages, but if you are already using another package manager like *conda*, that will work as well. To install *mamba*, download [mambaforge](https://github.com/conda-forge/miniforge#mambaforge) for your operating system.  If using Windows, be sure to check the box to "Add mamba to my PATH environment variable" to enable use of mamba directly from your command line interface. **Note that this may cause an issue if you have an existing mamba install through Anaconda.**  

## Python Environment Setup

These Python Environments will work for all of the guides, how-to's, and tutorials within this repository. A `.yml` file that can be used to set up the necessary environment has been included in the repository for both Windows and MacOS. Use the appropriate file in the steps below.

> If you wish to use *conda* as your package manager you can simply substitute 'conda' for 'mamba' in the steps below.

1. Using your preferred command line interface (command prompt, terminal, cmder, etc.) navigate to your local copy of the repository, then type the following to create a compatible Python environment.

    For Windows:

    ```cmd
    mamba env create -f setup/lpdaac_vitals_windows.yml
    ```

    For MacOS(tested on arm-64):

    ```cmd
    mamba env create -f setup/lpdaac_vitals_macos.yml
    ```

2. Next, activate the Python Environment that you just created.

    ```cmd
    mamba activate lpdaac_vitals 
    ```

3. Now you can launch Jupyter Notebook to open the notebooks included.

    ```cmd
    jupyter notebook 
    ```

If you're having trouble creating a compatible Python Environment or having an issue with one of the above environments, you can also try to create one using the commands below. Using your preferred command line interface (command prompt, terminal, cmder, etc.) type the following to create a compatible Python environment.

For Windows:

```cmd
mamba create -n lpdaac_vitals -c conda-forge --yes python=3.11 fiona=1.8.22 gdal hvplot geoviews rioxarray rasterio jupyter geopandas earthaccess jupyter_bokeh h5py h5netcdf spectral scikit-image
```

For MacOSX:

```cmd
mamba create -n lpdaac_vitals -c conda-forge --yes python=3.9 gdal=3.6.4 hvplot geoviews rioxarray rasterio geopandas fiona=1.8.22 jupyter earthaccess jupyter_bokeh h5py h5netcdf spectral scikit-image
```

After this, you should be able to do steps 2 and 3 above.

**Still having trouble getting a compatible Python environment set up? Contact [LP DAAC User Services](https://lpdaac.usgs.gov/lpdaac-contact-us/).**  

---

## Contact Info  

Email: <LPDAAC@usgs.gov>  
Voice: +1-866-573-3222  
Organization: Land Processes Distributed Active Archive Center (LP DAAC)¹  
Website: <https://lpdaac.usgs.gov/>  
Date last modified: 09-29-2023  

¹Work performed under USGS contract G15PD00467 for NASA contract NNG14HH33I.  
