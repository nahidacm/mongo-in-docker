# Mongo Chatsheet

## Git Clone
`git clone https://github.com/nahidacm/mongo-in-docker.git`

`cd mongo-in-docker`
## Start the docker container
`docker-compose up -d`

## Get into the container
`docker exec -it mongodb /bin/bash`

## Then get into mongodb console
`mongodb`

## Switch database
`use admin`

## Create mongo admin user

```javascript
db.createUser({
  user: "admin",
  pwd: "localadminpass",
  roles: [
            { role: "userAdminAnyDatabase", db: "admin" },
            { role: "readWriteAnyDatabase", db: "admin" },
            { role: "dbAdminAnyDatabase",   db: "admin" }
         ]
});
```
```javascript
db.createUser({
  user: "pmsusr",
  pwd: "pmspwdpass",
  roles: [
            { role: "userAdmin", db: "pms-360" },
            { role: "dbAdmin",   db: "pms-360" },
            { role: "readWrite", db: "pms-360" }
         ]
});
```

## Connection string

`mongodb://admin:localadminpass@localhost:27017/maasranga?authSource=admin&readPreference=primary&ssl=false`
