# Installing Jupyter Notebook

These instructions assume that you have miniconda installed in your home directory.

1. Log into the server

```bash
ssh USERNAME@okapi.math.unr.edu
```

1. Install the necessary packages for the conda environment

```bash
conda activate base
conda install jupyter jupyterlab nodejs
```

2. Create the jupyter config file

```bash
jupyter notebook --generate-config
```

3. *(optional, recommended)* Create a password for your notebook
- This can be a simple password
- Follow the prompt

```bash
jupyter notebook password
```
  - The hashed password will be saved in `~/.jupyter/jupyter_notebook_config.json`
  - Now is a good time to view the contents of the above file
  - Copy the hash starting with `sha1:`

4. Edit the config file. You can use `vim`, `vi`, `nano`, or your favorite terminal text editor

```bash
vim .jupyter/jupyter_notebook.config.py
```

- Edit the following 
  - **Default directory**: `c.NotebookApp.notebook_dir = '/home/USERNAME/DIR/'` *(optional)*
  - **Open browser**     : `c.NotebookApp.open_browser = False`
  - **Password**         : `c.NotebookApp.password = u'sha1:salt:hash'` *(hash generated from step 3)*
  - **Port**             : `c.NotebookApp.port = 9090` *(optional, recommended, default port=8888)*
