# kolorskemo.com

## Instructions

1. Create environment file
```sh
touch .env
```
Set `CERTBOT_DOMAINS` and `CERTBOT_EMAIL` appropriately.

2. Start the multi-container application.
```sh
$ docker-compose up -d
```
This will also start the HTTP edge server (non-SSL)
Main nginx instance will fail. This is expected.

3. Run certbot to get SSL set up.
```sh
$ docker-compose -f certbot.yml up
```

4. Restart containers
```sh
$ docker-compose down
$ docker-compose up -d
```

5. ?????

6. **PROFIT!**