---
title: "Conda Enviornment Setup "
date: 2020-08-27T14:38:06-04:00
---

Here's my workflow for working in Python across platforms (Windows, Linux, and HPC clusters)  
1. Install miniconda (Anaconda will do as well, but perhaps don't follow this workflow with Anaconda)  
2. conda config --add channels conda-forge #to make conda-forge default  
3. conda env update -f bidhya_environment.yaml #update everything from the yaml file  
4. conda update --all #I run it periodically to update everything to latest version; but new things break more often so take care  

## Sample Conda_env.yaml file
name:
channels:
  - conda-forge
  - default
dependencies:
  - scipy
  - pandas
  - matplotlib
  - scikit-learn
  - scikit-image
  - statsmodels
  - seaborn
  - lxml
  - beautifulsoup4
  - jupyter
  - jupyterlab
  - nltk
  - numba
  - astropy
  - bokeh
  - selenium #required for bokeh.io or saving with hvplot
  - phantomjs #for saving hvplot
  - bqplot
  - dill
  - mkl
  - mayavi
  - networkx
  - geopandas
  - cartopy
  - rasterio
  - georasters
  - geoplot
  - geopy
  - spectral
  - h5py
  - pytables
  - eccodes
  - cfgrib
  - xarray
  - intake
  - intake-xarray
  - intake-stac
  - hvplot
  - panel
  - earthpy
  - s3fs
  - dask
  - dask-ml
  - mplleaflet
  - ipyleaflet
  - wrf-python
  - regionmask
  - psyplot
  - psy-maps
  - psyplot-gui
  - psy-reg
  - py6s #atmorpheric correction
  - deap #GA (alternative : pyevolve)
  - python-docx #: for  wordcloud 
  - wordcloud
  - ipympl
  - podaacpy
  - pycrs
  - zarr
  - tqdm
  - cython
  - flask
  - cftime
  - datashader
  - datashape
  - geoviews #-core # geoviews only creates conflict with netCDF4 on windows; now pip install geoviews for 1.8 version
  - html5lib
  - nodejs
  - xlrd
  - urbanaccess
  - pandana
  - pysheds
  - gmaps # to use google maps instead of leaflet; need api key
  - geojsonio
  - cdsapi
  - joblib
  - matplotlib-scalebar
  - python-graphviz
  - rio-cogeo
  - sat-search
  - sat-stac
  - pystac
  - earthengine-api
  - fsspec
  - gcsfs
  - awscli
  - nodejs
  - pyarrow
  - vaex
  - ipyvuetify
  - plotly
  - ipyvolume
  - ipywidgets
  - pysolar
  - rioxarray
  - tpot
  #- spyder  
  - pip
  - pip:
    - laspy    
    - Pydap
    - siphon
    - metpy
    - eo-learn
    - keplergl
    - mimesis
    - topojson
    - salem
    - s2cloudless
    - planet  

Aside: [about me](/about)  
