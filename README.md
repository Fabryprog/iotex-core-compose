# iotex-core-compose

Docker compose to create a IoTeX node (testnet)	

# Config file

you must change using yoir public ip


```

nodeType: "full_node"

network:
    host: PUBLIC_IP_HERE 
    port: 30555
    bootstrapNodes:
        - "bootnode.iotexconnect.io:30555"

chain:
    chainDBPath: "./db/chain.db"
    trieDBPath: "./db/trie.db"
    producerPrivKey: "925f0c9e4b6f6d92f2961d01aff6204c44d73c0b9d0da188582932d4fcad0d8ee8c66600"
    producerPubKey: "336eb60a5741f585a8e81de64e071327a3b96c15af4af5723598a07b6121e8e813bbd0056ba71ae29c0d64252e913f60afaeb11059908b81ff27cbfa327fd371d35f5ec0cbc01705"
    enableFallbackToFreshDb: true
    enableSubChainStartInGenesis: false

consensus:
    scheme: "NOOP"
    blockCreationInterval: 2s

blockSync:
    interval: 1s

system:
    httpProfilingPort: 6060
    httpMetricsPort: 8080

explorer:
    enabled: true

```

# Test

```

curl -X POST --data '{"jsonrpc":"2.0","method":"Explorer.getBlockchainHeight","params":[],"id":"1"}' 127.0.0.1:14004 

```
