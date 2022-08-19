# journey

git clone https://github.com/Rancune/journey.git

git submodule update --init --recursive

npm install

code .

docker compose up

To dump the database:
docker exec <mongodb container> sh -c 'mongodump --authenticationDatabase admin -u <user> -p <password> --db <database> --archive' > db.dump

To restore the database:
docker exec -i <mongodb container> sh -c 'mongorestore --authenticationDatabase admin -u <user> -p <password> --db <database> --archive' < db.dump


