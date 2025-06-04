```bash
docker run --name inspircd -e "INSP_NET_SUFFIX=.domain.com" -e "INSP_NET_NAME=SB Network"
-e "INSP_SERVER_NAME=irc.domain.com" -e "INSP_ADMIN_NAME=Name" -e "INSP_ADMIN_DESC=TechiGuy"
-e "INSP_ADMIN_EMAIL=re@domain.com" -e "INSP_CONNECT_PASSWORD=\$2a\$10\$......."
-e "INSP_CONNECT_HASH=bcrypt"  -e "INSP_OPER_HASH=bcrypt" -e "INSP_OPER_PASSWORD_HASH=\$2a\$10\$0......"
-e "INSP_TLS_CN=irc.domain.com" -e "INSP_TLS_MAIL=re@domain.com"
-e "INSP_TLS_UNIT=Name" -d -p 6697:6697  -v ./inspircd:/inspircd/conf/
--restart=always inspircd/inspircd-docker:4.7.0
```

- Use ``bcrypt`` to hash your password and use excape character ``\`` for special characters ``$,@...``
- In the above example, I use self-signed certificates but it is possible to use your certificate. ( See the image docker hub page )
