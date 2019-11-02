# Connecting to the Jupyter Notebook

1. Connect to the server with port forwarding

```bash
ssh -L 9090:localhost:9090 USERNAME@okapi.math.unr.edu
```

2. Open up a jupyter notebook
```bash
conda activate base
jupyter notebook
```
  - Read the output of the server. If you set up a password, you can skip to step 4

3. Copy the jupyter notebook address that contains the token
  - It will look something like 
    - `http://localhost:8888/?token=58479cde25979cd3ecd85932969e2e9b0fa931c71452a822`
  - Copy this address (from your own terminal) and go to the next step
    - Make sure to use `Ctr+Shift+C` to copy
  
4. Open up a browser on your local machine
  - If you set up a password, then navigate to `localhost:9090`
  - If not, paste the address that you copied in step 3