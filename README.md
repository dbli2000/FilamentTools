# FilamentTools
 Tools for processing cryoEM data of filaments. 
 - FiTSuite_typecluster allows for clustering and selection of particle groups
 - FiTSuite_summarygenerator produces dataset summaries once types are separated (and optionally map slices after refinement/post-processing)

Note that this is not yet compatible with the newly released Jupyter Notebook 7, so either stick with 6 or try NbClassic (not yet tested). 

All scripts are self-contained, but in order to avoid dependency errors it is probably a good idea to use a virtual environment set up either with venv or conda. An example of one way to set up such a virtual environment is below:


## Virtual Environment Setup
### *General instructions*
The following is a simple way to set up an virtual environment with venv if you don't know how to:
- Run the following commands in a new terminal, then shutdown your current jupyter notebook and server
    - `python3 -m venv FiTSuite`
    - `source FiTSuite/bin/activate.csh` or `source FiTSuite/bin/activate`
    - `python3 -m pip install ipykernel`
    - `python3 -m ipykernel install --user --name=FiTSuite`
- Re-run the command `jupyter notebook` or `python3 -m notebook` or whatever you normally do and open this notebook
    - Currrently incompatible with JupyterLab 4 due to plotly issues... use JupyterLab 3 e.g. `pip install jupyterlab==3`
- Upon reopening, choose FiTSuite as Kernel by going to `Kernel > Change kernel > FiTSuite`

When done running the Jupyter notebook and shutting down the server, you can deactivate the virtual environment with `deactivate` in the second terminal

After you have done this once, next time just run `jupyter notebook` to get back here, and change kernel to `FiTSuite` again

### *LMB instructions*
The following is a simple way to set up an virtual environment with venv if you don't know how to:
- Run the following commands in a new terminal from your LMB home directory:
    - `module avail python`
        - Should see something like "python3/3.10.7" or higher
    - `module load python3/3.10.7` 
        - or whatever the latest version of python is
    - `python3 -m venv FiTSuite`
    - `source FiTSuite/bin/activate.csh` or `source FiTSuite/bin/activate`
    - `python3 -m pip install jupyter notebook` (could also be pip3)
        - Currrently incompatible with JupyterLab 4 due to plotly issues... use JupyterLab 3 e.g. `pip install jupyterlab==3`        
    - `python3 -m ipykernel install --user --name=FiTSuite`
- Run the command `jupyter notebook` or `python3 -m notebook` or whatever you normally do and open this notebook
- Upon reopening, choose FiTSuite as Kernel by going to `Kernel > Change kernel > FiTSuite`

When done running the Jupyter notebook and shutting down the server, you can deactivate the virtual environment with `deactivate`

After you have done this once, next time just reactivate the virtual environment, run `jupyter notebook` to get back here, and make sure kernel is still set to `FiTSuite`

Also, can source from my home directory -> `source lmb/home/dli/FiTSuite/bin/activate.csh`. This is likely easiest...
