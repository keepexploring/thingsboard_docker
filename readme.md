Creating a thingsboard instance with the postgres database in a separate container

Install the above

Install docker image of timescaledb
sudo docker run -d --name thingsboard-timescaledb -p 5433:5432 timescale/timescaledb --restart unless-stopped
see https://github.com/timescale/timescaledb-docker for more info (I've just changed the exposed port on the host)

now cd into the folder with the docker files from the repro in and run
docker-compose up -d tb

and this should start thingsboard

