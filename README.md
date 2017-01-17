# Fast-Datalab

1. 
Pour démarrer votre notebook Jupyter

```bash

docker build -t fast-datalab .
docker run -p 8888:8888 --rm fast-datalab

```

2. Rendez-vous ensuite sur l'URL affichée dans votre terminal
Elle sera sous cette forme: http://localhost:8888?token=<sequence of digits>


Pour monter un volume externe:


```bash

docker run -p 8888:8888 \
           --rm \
           -u $(id -u):$(id -g) \
           -v `pwd`:/home/jupyteruser/work \
           fast-datalab

```
