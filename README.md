infogramma
==========

Initialize the notebook env:

```
# Build the docker image for this repo
docker build -t hidinginabunker/infogramma .
# Run this image and mount the notebooks folder to this dir
docker run -d -p 443:8888 -e "PASSWORD=MakeAPassword" -v $PWD/notebooks:/notebooks hidinginabunker/infogramma
```

If you're boot2dockerin' on osx, then the server is now exposed on the port of your VM:
```
echo https://`boot2docker ip 2> /dev/null | cut -d":" -f2`
```

TODO:
- Fix websocket connection failing
