infogramma
==========

## Initialize the notebook env

```
# Build the docker image for this repo
docker build .
# Run this image and mount the notebooks folder to this dir
docker run -d -p 443:8888 -e "PASSWORD=password" -v $PWD/notebooks:/notebooks ipython/scipyserver
```

If you're boot2dockerin' on osx, then the server is now exposed on the port of your VM:
```
echo https://`boot2docker ip 2> /dev/null | cut -d":" -f2`
```


## Viewing Notebooks
http://nbviewer.ipython.org/github/hidinginabunker/infogramma/tree/master/notebooks/


Issues:
- Websockets fail in safari


