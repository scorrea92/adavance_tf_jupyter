# Advance Tensorflow in Jupyter
Some POCs of advances DL models in TF

## Mac Instalation

It is possible to install and run Python/TensorFlow entirely from your Mac, without the need for Google CoLab. Running TensorFlow locally does require some software configuration and installation. If you are not confortable with software installation, just use Google CoLab.

The first step is to install Python 3.10. As of January 2023, this is the latest version of Python 3. I recommend using the [Miniconda (Anaconda) release of Python](https://docs.conda.io/en/latest/miniconda.html), as it already includes many of the data science related packages that are needed by this class. Anaconda directly supports Windows, Mac, and Linux. Miniconda is the minimal set of features from the extensive Anaconda Python distribution. Download Miniconda from the following URL:

Next, you should install the xcode-select command-line utilities. Use the following command to install:

```bash
xcode-select --install
```

## Install Jupyter and Create Environment

Next, lets install Jupyter

```bash
conda install -y jupyter
```

First, we deactivate the base environment.
```bash
conda deactivate
```

Next, we will install the conda eviroment using the experimentation.yml file.
```bash
conda env create -f experimentation.yml -n tensorflow
```

## Activating New Environment
To enter this environment, you must use the following command:
```bash
conda activate tensorflow
```

## Register your Environment
The following command registers your tensorflow environment. Again, make sure you "conda activate" your new environment.
```bash
python -m ipykernel install --user --name tensorflow --display-name "Python 3.10 (tensorflow)"
```