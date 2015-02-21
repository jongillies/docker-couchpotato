#docker couchpotato

This is a Dockerfile to set up "CouchPotato" - (https://couchpota.to/)

Build from docker file

```
git clone https://github.com/jongillies/docker-couchpotato.git
cd docker-couchpotato
docker build -t couchpotato .
```

docker run -d  \
    -v $COUCHPOTATO_CONFIG:/config \
    -v $COUCHPOTATO_DATA:/data \
    -v $MOVIE_LIBRARY_DIR:/movies \
    -v $COUCHPOTATO_COMPLETE:/complete \
    -p 5050:5050 --name couchpotato couchpotato


When filling out the CP wizard, check the Rename downloaded movies.

From should be /complete
To   should be /movies

