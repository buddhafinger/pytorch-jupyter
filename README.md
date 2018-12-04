What the hell is this?

A quick hash of pytorch docker container that I modified to include jupyter. - Make sure to read through to the bottom for the super cool tips section. 

To use this neat little bundle of love simply type
#'docker-compose up' 

To stop it run
docker-compose stop

To delete it run
#docker-compose down
all commands need to be from the root directory of this project.


Once it's running ...
Then browse to localhost:8888

The password is listed in the README.md file in the .jupyter folder - YOU SHOULD CHANGE THIS.

Data:
Persistent data will be stored in
/workspace	#storage for notebooks
/.jupyter       #maps to .jupyter config dir on container.


How???
I took a copy of the main pytorch image with 
#docker pull pytorch/pytorch' 
Jumped onto the running containing and installed jupyter from the container commandline like so 
#conda install -c anaconda jupyter

Then saved changes to the container and pushed it up to my buddhafinger repo. 

https://hub.docker.com/r/buddhafinger/pytorch-jupyter/ 

Is this even the correct way to do this stuff?  - Don't know, but learnt a few things about notebooks when setting it up and will go from there.




What's next?
Maybe extend notebook features with added plugins.


Useful links:

https://jupyter-notebook.readthedocs.io/en/stable/public_server.html#running-a-public-notebook-server

https://pytorch.org/tutorials/

Super cool tips!

Module not installed?  No worries, install modules from within the notepad!!!
# Install a conda package in the current Jupyter kernel
import sys
!conda install --yes --prefix {sys.prefix} numpy

#Note - The modules will exist as long as the container does, if you delete the container (not the image) you lose the updated modules, to get around this you can write docker changes to your local imaGE. You can google how to that.








