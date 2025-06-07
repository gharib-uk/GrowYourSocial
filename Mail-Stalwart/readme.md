```bash
docker run -d  -p 443:443 -p 8080:8080 -p 25:25 -p 587:587 -p 465:465 \
-p 143:143 -p 993:993 -p 4190:4190 -p 110:110 -p 995:995 \
-v ./stalwart:/opt/stalwart --name stalwart stalwartlabs/stalwart:latest
```

```
$ docker logs stalwart
✅ Configuration file written to /opt/stalwart/etc/config.toml
🔑 Your administrator account is 'admin' with password 'w95Yuiu36E'.
```

Follow the instructions in this [link](https://stalw.art/docs/install/platform/docker/)
