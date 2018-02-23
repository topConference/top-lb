# top
loopback

mongo -u 00 -p dilidili 159.89.128.65/topconference
use topconference

db.createUser({
    user: '0',
    pwd: 'dilidili',
    roles: [{ role: 'readWrite', db:'topconference'}]
})

mongo "mongodb://cluster0-shard-00-00-kxonx.mongodb.net:27017,cluster0-shard-00-01-kxonx.mongodb.net:27017,cluster0-shard-00-02-kxonx.mongodb.net:27017/test?replicaSet=Cluster0-shard-0" --authenticationDatabase admin --ssl --username bilibili --password dilidili

npm install --save loopback-connector-mongodb
npm install -g loopback-cli
lb datasource mongoDS --connector mongoDB
lb model
