# docker-ds
Container For Machine Learning Experiments

This is docker image for Python3, Jupyter and Octave, based on alpine linux

Useful packages included:
1. Pandas: import data via a url and create a dataframe to easily handle data for analysis and graphing. See examples of using Pandas here: https://plot.ly/pandas/.
2. NumPy: a package for scientific computing with tools for algebra, random number generation, integrating with databases, and managing data. See examples of using NumPy here: https://plot.ly/numpy/.
3. SciPy: a Python-based ecosystem of packages for math, science, and engineering.
4. Plotly: a graphing library for making interactive, publication-quality graphs. See examples of statistic, scientific, 3D charts, and more here: https://plot.ly/python.

### Run
You can run the command below:

```bash
git clone https://github.com/rajasoun/docker-ds
docker-compose up  -d
```

To start Only Jupyter Notebook:

```bash
docker-compose  up jupyter
```

visit 
1. [http://localhost:18888](http://localhost:18888) for jupyter notebook
2. [http://localhost:18989](http://localhost:18989) for jupyter notebook Viewer



### Manage Docker via Web - [Portainer](https://portainer.io/)

Visit [http://localhost:19090](http://localhost:19090) for Docker Management