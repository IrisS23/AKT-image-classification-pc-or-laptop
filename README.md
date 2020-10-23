# Laptop or PC

Using tensorflow a classifier should be created that can categorize images as either laptops or PCs.

## Docker
- Navigate to main directory of the repository
- Run command:  
`docker run -it --rm -v ${PWD}:/home/jovyan/work -p 8888:8888 jupyter/tensorflow-notebook`


(docker image `tensorflow/tensorflow:latest-jupyter` does not work because `scipy` is not installed)