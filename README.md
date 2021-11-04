## Set-up
Once the Elasticsearch instance is deployed, use a [`jupyter-minimal`](https://hub.docker.com/r/jupyter/minimal-notebook/tags/) docker image to run Jupyter notebook locally. It comes with many packages already installed.

Start by connecting the current working directory to the Docker container:
```
$ docker run -p 8888:8888 -v $(pwd):/home/jovyan/work jupyter/minimal-notebook 
```
To install required packages, enter the docker container:
```
$ docker exec -it CONTAINER-ID /bin/bash
```

then use `pip` to install the following libraries :
```
elasticsearch==7.15.1
elasticsearch-dsl==7.4.0
pandas==1.3.4
requests==2.26.0
seaborn==0.11.2
matplotlib==3.4.3
ipython-autotime==0.3.1
```

If not, use a simple virtual environement and `pip install` the `requirements.txt`.

## Answers

The `company_search.ipynb` contains the entire exercice and is organised in two main sections:

1. EDA(Exploratory data analysis): where I explore and get to know the data a little.
2. Elasticsearch: where I connect to the ES server, index and then query the data.

The notebook is commented which explain the major implementation choices.