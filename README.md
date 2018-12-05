# iotex-core-compose

Docker compose to create a IoTeX node (testnet)	

The compose has:
1. iotex-core image
2. iotex-explorer image

# Config file

copy the file ```config.template.yml``` into ```config.yml``` and edit it. You must change using yoir public ip

# Start your node

```
docker-compose up -d
```

# Test your node

## Request

```
curl -X POST --data '{"jsonrpc":"2.0","method":"Explorer.getBlockchainHeight","params":[],"id":"1"}' 127.0.0.1:14004 
```

## Response

```
{"jsonrpc":"2.0","id":"1","result":231746}
```
# Explorer

You can open the explorer using this url: http://<YOUR IP>:4004/
