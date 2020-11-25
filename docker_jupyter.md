start jupyter notebook container on remote server with forwarded port 8000
```bash
docker run -p 8000:8888 jupyter/minimal-notebook
```

in local browser use
localhost:8000

to log in use the token from remote server

name a container
datascience container also has R and Julia and a lot of packages preinstalled
```bash
docker run -p 8000:8888 --name datascience jupyter/datascience-notebook
```

other useful commands
```bash
docker container list all

docker container rm 

docker container prune

docker container logs
```

access a runing docker container
```bash
docker container exec -it container_name
```

bcl2fastq container
```bash
docker pull quay.io/biocontainers/bcl2fastq-nextseq:1.2.6--py_0
```

to_run (https://github.com/brwnj/bcl2fastq):
```bash
docker run quay.io/biocontainers/bcl2fastq-nextseq:1.2.6--py_0 bcl_to_fastq -h
```

blastp container
```bash
docker run biocontainers/blast:2.2.31 blastp -help
```

container runing interaktive python 3.9
```bash
docker run -v $pwd/my_research:/my_research -it python:3.9.0rc1-buster
```

run a python script with the container above and then remove container
```bash
docker run --rm -v $(pwd)/my_research:/my_research python:3.9.0rc1-buster python /my_research/new_python_example.py
```

create an image from a container
```bash
docker comit mycontainer myimagename
```

start a container
```bash
docker container start <container_name>
```

making and building a images
```bash
docker build . 

docker build . --tag
```

Pushing to docker hub
```bash
docker login --username=yourhubusername --email=youremail@company.com
docker images
docker tag image_id yourhubusername/verse_gapminder:firsttry
docker push yourhubusername/verse_gapminder
```



