# Work on Remote Server
Tips and cookbooks related to working on a remote server.

### Run graphical Linux applications on Windows 10
https://seanthegeek.net/234/graphical-linux-applications-bash-ubuntu-windows/

### ssh login

        ssh username@remote_server

### Inquire information from netCDF files

        ncdump -h xxxx.nc

### Quick visualization of netCDF files

        ncview xxxx.nc


### ssh login without tying password
1. generate the keys (private + public)

        ssh-keygen -t rsa
> all use the defaults settings.

2. copy the  public key to the remote server

        ssh-copy-id username@remote_server

### Open Jupyter notebook on remote server and access it at local machine
1. Remote server terminal

        jupyter-notebook --no-browser --port=8899 --ip=127.0.0.1
> port 8899 might be unavailable, in which case a different port # may be used.


2. Local machine terminal

        ssh -NL localhost:8888:localhost:8899 remote_server
> use the assigned port number in step 1 to replace 8899 when applicable.

3. Local machine browser

        http://localhost:8888

### The jupyterhub server at Princeton
[https://github.com/Resplandy/climate-hpc/blob/master/jupyterhub.md](https://github.com/Resplandy/climate-hpc/blob/master/jupyterhub.md)
