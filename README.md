# ou-m269-unofficial
M269 unofficial testing repo


[![Binder](https://mybinder.org/badge_logo.svg)](https://gke.mybinder.org/v2/gh/ouseful-course-containers/ou-m269-unofficial/master)

This repository demonstrates a computing environment that is appropriate for the practical activities for the updated version of the OU course M269 due for release in 202x.

A Docker container image built from the repository using `repo2docker` is available on Dockerhub: [`ousefuldemos/ou-m269-unofficial`](https://hub.docker.com/repository/docker/ousefuldemos/ouseful-course-containers/ou-m269-unofficial)

## Getting Started
You can explore the contents of this repository via interactive Jupyter notebooks by clicking the *Binder* button above.

To run the environment on your own computer, you need to do the following:

- install Docker onto your computer; you can download the installation files from the Docker website: [Get Docker](https://docs.docker.com/get-docker/)

- open a terminal / command prompt in your desktop; from the command prompt, do the following:
  - create a working directory / folder to work in by entering the command: `mkdir M269`;
  - change directory into that fold by running the command: `cd M269`;
  - launch the docker container by running the command: `docker run --name m269test -p 8269:8888 -v $PWD:/home/jovyan/notebooks  -e JUPYTER_TOKEN="letmein" ousefuldemos/ouseful-course-containers/ou-m269-unofficial:latest`
  - stop (hibernate) the container with the command: `docker stop m269test`
  - restart the container with the command: `docker restart m269test`
  
When you run the `docker` command, several things will happen:
 
 - first, docker will download the container image from DockerHub (this may take some time but only happens the first time you try to run the container);
 - then, docker will launch the container and a Jupyter notebook server will start running inside it.
 
When the container is running, go to [`localhost:8129`](http://localhost:8129) in your browser (if that doesn't work, try [`127.0.0.1:8269`](http://127.0.0.1:8269)) and you should see a running notebook server there.

Use the token `letmein` to access the server (you should only need to do this once).
 
Any files in the local `M269` directory on your host computer should appear in the `notebooks` folder in the notebook homepage directory listing.
