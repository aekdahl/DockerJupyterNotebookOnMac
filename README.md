# Run clean Jupyter Notebooks on Mac using Docker

A simple way to keep clean setups of python and jupyter using Docker.

1. Install the [Docker Desktop app](https://docs.docker.com/desktop/setup/install/mac-install/)
2. Open the Docker Desktop app and open a terminal window
3. Download an image with Jupyter notebook
```
docker pull jupyter/scipy-notebook
```
3. Create a project folder
```
mkdir ~/Docker
```
4. Launch the container
```
docker container run --name jupyter -p 8888:8888 -v ~/Docker:/home/jovyan/ jupyter/scipy-notebook
```
5. Find and copy the URL from the docker logs to the browser
