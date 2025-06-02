```
curl -fsSL https://get.docker.com -o install-docker.sh

docker compose run --rm -e SYNAPSE_SERVER_NAME=domain.com -e SYNAPSE_REPORT_STATS=yes synapse generate

docker exec -it register_new_matrix_user -c homeserver.yaml  synapseme
```
