# Hyperledger Fabric Based Trade Network

### Install Dependencies

```
npm install
npm install -g passport-github
```

### Re-generate your Business Network archive (BNA)

```
composer archive create --sourceType dir --sourceName . -a ./dist/my-network.bna
```


### Deploy the Business Network Definition to the runtime Fabric

```
cd ./dist
composer network deploy -a my-network.bna -p hlfv1 -i PeerAdmin -s randomString
```

### Generate the REST APIs for the updated Business Network

```
cd ..
composer-rest-server -p hlfv1 -n my-network -i admin -s adminpw -a true
```



