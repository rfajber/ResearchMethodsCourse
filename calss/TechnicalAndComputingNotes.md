# Technical and Computing Notes 

- The purpose of this document is to list some of the technical details that you will need in order to do the course, and show you where to find things you might need. 

## Course notes
 - The course notes will be posted in 3 places
   - as ipython notebooks on jupyterhub
   - as html previews on github
   - as pdfs of the html previews on mycourses
 - the course notes are themselves ipython notebooks, and are designed to have computing examples in them that you can run on and experiment with. I would encourage you to open them in jupyterlab (either on the hub or on your computer) and experiment with the code cells as you read through the notes. 

## MyCourses 
- The syllabus, course schedule, and project description will all be posted to mycourses. 
- I will also be posting pdfs of the course notes, but I would reccomend that you look at them with Jupyter Lab.

## Jupyterhub
- The jupyterhub is located at https://jhub.science.mcgill.ca 
- you will need to login with your mcgill credentials
- use the ATOC 557 environment 
- the files for the course are in a read only directory /home/shared/ResearchMethodsCourse
- if you open a terminal in your home directory and do ```ln -s ../shared .``` this will create a symbolic link to the shared folder in your own directory, which you will need to do in order to open the files. You should only need to do this once.

## Github 
- The labs, data, and course notes are available on github: https://github.com/rfajber/ResearchMethodsCourse
- I have not set up any fancy permissions, so please do not try to make any pull requests without specific permission.
- You can download these as a zip file if you are unfamiliar with git 
- if you are familiar with git you can init a new local repo and then add the remote using ```git remove add origin https://github.com/rfajber/ResearchMethodsCourse.git```
  - after you can pull the main branch with ```git pull main```

## Using your own computer
- you are welcome to use your own computer instead of jupyterhub, but I make no promises that it will work
- If you do not have a conda python environment set up on your computer already:
  - download miniconda: https://docs.conda.io/projects/miniconda/en/latest/
  - run the installer. You may need to restart your terminal after the installer completes.
  - (optional): create a new environment for your packages ```conda create --name myenv``` where myenv is a name you want to use. 
    - you can activate your new environment with conda activate p3
  - install the following packages:
    - ``` conda install numpy matplotlib scipy jupyter xarray netcdf dask pandas ```
    - the jupyterhub environment has a couple other packages installed, but this is the basic "stack" that I use. 
  - launch a local instance of jupyter lab with ```jupyter lab```
- If you already have a conda environment you can repeat the same steps as above, but I would recommend that you create a separate environment first.
- I would reccomend that you use a git repository if you are going to do things on your local machine.

## Computing tutorials
- More examples with Numpy: https://aaltoscicomp.github.io/python-for-scicomp/numpy/ (the other tutorials are also pretty good)
- If you are unsure about how xarray works: https://tutorial.xarray.dev/overview/xarray-in-45-min.html
- if you want to parallelize something without using dask: https://chriskiehl.com/article/parallelism-in-one-line 
- 
## Data Sources you might want to check out 
- much of the data that I used for this course came from the gridded datasets here: https://psl.noaa.gov/data/gridded/
- Canadian weather station data can be downloaded from here: https://climate.weather.gc.ca/historical_data/search_historic_data_e.html
- ocean bouy data can be found here: https://www.ndbc.noaa.gov/
- ERA5 reanalysis can be found here: https://www.ecmwf.int/en/forecasts/dataset/ecmwf-reanalysis-v5
- ORAS5 reanalsis can be found here: https://cds.climate.copernicus.eu/cdsapp#!/dataset/reanalysis-oras5?tab=form
- if you are planning on using a large dataset (>10GB) on jupyterhub please let me know and I can see if there is a better way to download it for you. 