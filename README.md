# FilamentTools
 Tools for processing cryoEM data of filaments. 
 - FiTSuite_typecluster allows for clustering and selection of particle groups
  - Can run on RELION Class2D or Select jobs post 2D classification
  - Example processing, data, and, output provided in FiTSuite, ExampleData, and ExampleOutput folders respectively
  - Run time < 1 minute on a 2017 MacBook pro, even faster on a Linux Cluster.
 - FiTSuite_summarygenerator produces dataset summaries once types are separated (and optionally map slices after refinement/post-processing) (up soon)

Note that this is not yet compatible with the newly released Jupyter Notebook 7, so either stick with 6 or try NbClassic (not yet tested). Have tested on Mac, Macbook, and Unix systems. 

Should be ready to go once you clone/download the repo. All scripts are self-contained, but in order to avoid dependency errors it is probably a good idea to use a virtual environment set up either with venv or conda. An example of one way to set up such a virtual environment is below:


## Virtual Environment Setup
### *General instructions*
The following is a simple way to set up an virtual environment with venv if you don't know how to:
- Run the following commands in a new terminal
    - `python3 -m venv FiTSuite`
    - `source FiTSuite/bin/activate.csh` or `source FiTSuite/bin/activate`
    - `python3 -m pip install -U -r requirements.txt` (with the correct path to the requirements.txt in this repo, could also be pip3)
    - `python3 -m ipykernel install --user --name=FiTSuite`
- Run the command `jupyter notebook` or `python3 -m notebook` or whatever you normally do and open this notebook
    - If you choose to just install jupyterlab, FiTSuite is currrently incompatible with JupyterLab 4 due to plotly issues... use JupyterLab 3 e.g. `pip install jupyterlab==3`
- Upon reopening, choose FiTSuite as Kernel by going to `Kernel > Change kernel > FiTSuite`

When done running the Jupyter notebook and shutting down the server, you can deactivate the virtual environment with `deactivate` in terminal

After you have done this once, next time just run `jupyter notebook`, and change kernel to `FiTSuite` again

### *LMB instructions*
The easiest way is to source from my home directory -> `source /lmb/home/dli/FiTSuite/bin/activate.csh`. Then run `jupyter notebook` and open the file

The following is a simple way to set up an virtual environment with venv if you don't know how to:
- Run the following commands in a new terminal from your LMB home directory:
    - `module avail python`
        - Should see something like "python3/3.10.7" or higher
    - `module load python3/3.10.7` 
        - or whatever the latest version of python is
    - `python3 -m venv FiTSuite`
    - `source FiTSuite/bin/activate.csh` or `source FiTSuite/bin/activate`
    - `python3 -m pip install -U -r requirements.txt` (with the correct path to the requirements.txt in this repo, could also be pip3)
    - `python3 -m pip install jupyter notebook` (could also be pip3)
        - If you choose to just install jupyterlab, FiTSuite is currrently incompatible with JupyterLab 4 due to plotly issues... use JupyterLab 3 e.g. `pip install jupyterlab==3`       
    - `python3 -m ipykernel install --user --name=FiTSuite`
- Run the command `jupyter notebook` or `python3 -m notebook` or whatever you normally do and open the notebook
- Upon reopening, choose FiTSuite as Kernel by going to `Kernel > Change kernel > FiTSuite`

When done running the Jupyter notebook and shutting down the server, you can deactivate the virtual environment with `deactivate`

After you have done this once, next time just reactivate the virtual environment, run `jupyter notebook` to get back here, and make sure kernel is still set to `FiTSuite`
