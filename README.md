This role installs Jupyter (previously ipython notebook), JupyterHub and sudospawner using Python 3.
 
It was developed and tested with Ubuntu 15.04, but should work on any recent Ubuntu or Debian.

This was tested on Scaleways (scaleway.com) and Digital Ocean. So it *does* work on ARM!

JupyterHub is installed as per instructions, with node.js and configurable-http-proxy.

To add a user, login to the server as root:

adduser <username>
addgroup <username> jupyter

Then connect via web browser

http://<ip address>:8000

For testing use this:

    ansible-playbook ansible-jupyterhub/test/test.yml -i ansible-jupyterhub/test/hosts

And configure jupyterhub your ssh/config file.
