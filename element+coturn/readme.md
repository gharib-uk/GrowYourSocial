```
curl -fsSL https://get.docker.com -o install-docker.sh

docker compose run --rm -e SYNAPSE_SERVER_NAME=domain.com -e SYNAPSE_REPORT_STATS=yes synapse generate

docker exec -it register_new_matrix_user -c homeserver.yaml  synapseme
```

```
# Configure PostgreSQL DB
database:
  name: psycopg2
  args:
    user: synapse
    password: synapseMainHelloHere
    database: synapse
    host: synapse-db #you can use docker inspect container_name to fill host section
    cp_min: 5
    cp_max: 10

```


```
turn_uris: ["turns:domain.comr:5349?transport=udp", "turns:domain.com:5349?transport=tcp", "turn:domain.com:3478?transport=udp", "turn:domain.com:3478?transport=tcp" ]
turn_shared_secret: 'shared_secret'
turn_user_lifetime: 864000
turn_allow_guests: false
```
