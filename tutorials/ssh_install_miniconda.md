# Installing miniconda via ssh

**Make sure that you have access to the Okapi server**

## Setup

1. Log in to the Okapi server through a terminal on your PC

```{bash}
ssh USERNAME@okapi.math.unr.edu
```

2. Download and install `miniconda`

```{bash}
cd ~/Downloads
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
sh Miniconda3-latest-Linux-x86_64.sh
```

  - Read the EULA and type 'yes' (hit `q` to skip reading)
  - Install in the default location (home directory) [ENTER]
  - Let conda initialize the environment

3. Log out and log back in
  - You should see the text `(base)` by your user name. If not, type `conda activate base`
  - This means that you are in the conda base environment
  - Any conda packages installed will go to this environment unless you have activated another one