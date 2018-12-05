
# pytorch jupyter

<div class="alert alert-block alert-info">
<b>What is this?:</b> A quick hash of pytorch docker container that I modified to include jupyter. Make sure to read through to the bottom for tips section.
</div>

To use this neat little bundle of love..

#### to start
'docker-compose up'

#### To stop 
'docker-compose stop

#### To Delete
'docker-compose down

All commands need to executed from the root directory of this project.

<div class="alert alert-block alert-info">
<b>Why would I want to use this?:</b> Exploring use of Pytorch with Jupyter using Docker magic.
</div>

After starting with docker compose then Then browse to http://localhost:8888

The password is listed in the README.md file in the .jupyter folder - YOU SHOULD CHANGE THIS.

<div class="alert alert-block alert-info">
<b>Data:</b> Persistent data will be stored in /workspace for notebooks and  /.jupyter for .jupyter config dir on container
</div>

Persistent data stores setup for exiting and new files that can be modified by the container.

<div class="alert alert-block alert-info">
<b>Data:</b> How did you make this?

I took a copy of the main pytorch image with 'docker pull pytorch/pytorch' 

Jumped onto the running containing and installed jupyter from the container commandline like with:
conda install -c anaconda jupyter

Then saved changes to the container and pushed it up to my buddhafinger repo.

https://hub.docker.com/r/buddhafinger/pytorch-jupyter/

Once I created and modified the jupyter config file I then wrapped it with docker-compose.

<div class="alert alert-block alert-info">
<b>Data:</b> What's next? Maybe extend modules and support in docker container and provide some handy examples.

<div class="alert alert-block alert-info">
<b>Tips?</b> Somevhandy tip(s) below.
</div>



import sys
!conda install --yes --prefix {sys.prefix} numpy

#Note - The modules will exist as long as the container does, if you delete the container (not the image) you lose the updated modules, to get around this you can write docker changes to your local image. You can google how to that.
