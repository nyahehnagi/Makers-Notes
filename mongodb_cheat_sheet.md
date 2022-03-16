`sudo rm /var/lib/mongodb/mongod.lock` Remove lock

`sudo mongod --fork -f /etc/mongod.conf` start up Mongodb

https://docs.mongodb.com/mongodb-shell/run-commands/


`ps -e | grep mongo` Prints the process detail of running mongo instance

`nc -v localhost 27017` Prints whether connection to mongodb running on port 27017 is succeeded