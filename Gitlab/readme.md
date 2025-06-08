- Use the ``docker-compose.yml`` to fire up your gitlab instance
- Use the following command to retrieve the password for ``root`` account
```bash
sudo docker exec -it gitlab grep 'Password:' /etc/gitlab/initial_root_password
```
