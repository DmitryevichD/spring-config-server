# Spring config server template

### [integration-schema](./C4-container-level.puml)

### How to receive config values
`curl http://localhost:8888/{application}/{profile}/{label(branch)}`

#### Examples:
default branch (production)<br>
`curl http://localhost:8888/client/default -u user:secret | jq .`<br>
or<br>
`curl http://localhost:8888/client/default/production -u user:secret  | jq .`

### How to use password encryption\decryption
#### Encrypt:
`curl -X POST http://localhost:8888/encrypt -u user:secret  -d 'your sensitive data'`
#### Decrypt:
`curl -X POST http://localhost:8888/decrypt -u user:secret -d 'your sensitive data'`
