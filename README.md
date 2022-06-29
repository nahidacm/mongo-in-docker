# Mongo Chatsheet
## Get into the container
`docker exec -it mongodb /bin/bash`

## Then get into mongodb console
`mongodb`

## Create mongo user

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

`mongodb://admin:localadminpass@localhost:28018/maasranga?authSource=admin&readPreference=primary&ssl=false`
