# Mongo Chatsheet

## Create mongo user


db.createUser({
  user: "admin",
  pwd: "localadminpass",
  roles: [
            { role: "userAdminAnyDatabase", db: "admin" },
            { role: "readWriteAnyDatabase", db: "admin" },
            { role: "dbAdminAnyDatabase",   db: "admin" }
         ]
});


db.createUser({
  user: "pmsusr",
  pwd: "pmspwdpass",
  roles: [
            { role: "userAdmin", db: "pms-360" },
            { role: "dbAdmin",   db: "pms-360" },
            { role: "readWrite", db: "pms-360" }
         ]
});`
`
