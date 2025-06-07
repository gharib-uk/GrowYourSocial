- Create admin user with the following command
```bash
docker exec -it CONTAINER_NAME_OR_ID \
    /gotosocial/gotosocial \
    admin account create \
    --username some_username \
    --email someone@example.org \
    --password 'some_very_good_password'
```
- Promote a normal user to admin
```bash
./gotosocial --config-path ./config.yaml admin account promote --username YOUR_USERNAME
```
