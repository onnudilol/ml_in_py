# Machine Learning in Python Jupyter Notebooks

This is a selection of Jupyter notebooks adapted from the code in Michael Bowle's [Machine Learning in Python](http://www.wiley.com/WileyCDA/WileyTitle/productCd-1118961749.html).
The code has been refactored to be Python 3.6 compatible, more closely follow PEP8, and fix deprecation warnings.

# Running the Code

### Virtualenvs

Create a virtual environment using [pipenv](https://github.com/pypa/pipenv):

`pipenv --python 3.6 install`

Create a kernel using `ipykernel`:

```pipenv run python -m ipykernel install --user --name=name_of_virtualenv```

Run Jupyter:

`jupyter notebook`

### Docker

Modify the permissions of the notebook directory:

`sudo chown 1000 /path/to/notebooks`

Pull the docker image:

`docker pull jupyter/scipy-notebook`

Run Jupyter:

`docker run -it --rm -p 8888:8888 -v /path/to/notebooks:/home/jovyan/work jupyter/scipy-notebook`