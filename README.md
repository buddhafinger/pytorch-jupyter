{
 "cells": [
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "# pytorch jupyter"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "<div class=\"alert alert-block alert-info\">\n",
    "<b>What is this?:</b> A quick hash of pytorch docker container that I modified to include jupyter. Make sure to read through to the bottom for tips section.\n",
    "</div>"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "To use this neat little bundle of love..\n",
    "\n",
    "#### to start\n",
    "'docker-compose up'\n",
    "\n",
    "#### To stop \n",
    "'docker-compose stop\n",
    "\n",
    "#### To Delete\n",
    "'docker-compose down\n",
    "\n",
    "All commands need to executed from the root directory of this project."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "<div class=\"alert alert-block alert-info\">\n",
    "<b>Why would I want to use this?:</b> Exploring use of Pytorch with Jupyter using Docker magic.\n",
    "</div>"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "After starting with docker compose then Then browse to http://localhost:8888\n",
    "\n",
    "The password is listed in the README.md file in the .jupyter folder - YOU SHOULD CHANGE THIS."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "<div class=\"alert alert-block alert-info\">\n",
    "<b>Data:</b> Persistent data will be stored in /workspace for notebooks and  /.jupyter for .jupyter config dir on container\n",
    "</div>"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "Persistent data stores setup for exiting and new files that can be modified by the container."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "<div class=\"alert alert-block alert-info\">\n",
    "<b>Data:</b> How did you make this?"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "I took a copy of the main pytorch image with 'docker pull pytorch/pytorch' \n",
    "\n",
    "Jumped onto the running containing and installed jupyter from the container commandline like with:\n",
    "conda install -c anaconda jupyter\n",
    "\n",
    "Then saved changes to the container and pushed it up to my buddhafinger repo.\n",
    "\n",
    "https://hub.docker.com/r/buddhafinger/pytorch-jupyter/\n",
    "\n",
    "Once I created and modified the jupyter config file I then wrapped it with docker-compose."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "<div class=\"alert alert-block alert-info\">\n",
    "<b>Data:</b> What's next? Maybe extend modules and support in docker container and provide some handy examples."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "<div class=\"alert alert-block alert-info\">\n",
    "<b>Tips?</b> Somevhandy tip(s) below.\n",
    "</div>"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "\n",
    "\n",
    "import sys\n",
    "!conda install --yes --prefix {sys.prefix} numpy\n",
    "\n",
    "#Note - The modules will exist as long as the container does, if you delete the container (not the image) you lose the updated modules, to get around this you can write docker changes to your local image. You can google how to that."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": []
  }
 ],
 "metadata": {
  "kernelspec": {
   "display_name": "Python 3",
   "language": "python",
   "name": "python3"
  },
  "language_info": {
   "codemirror_mode": {
    "name": "ipython",
    "version": 3
   },
   "file_extension": ".py",
   "mimetype": "text/x-python",
   "name": "python",
   "nbconvert_exporter": "python",
   "pygments_lexer": "ipython3",
   "version": "3.6.7"
  }
 },
 "nbformat": 4,
 "nbformat_minor": 2
}
