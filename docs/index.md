## local development

### assumptions
- ollama is installed locally and running at `http://localhost:11434`
- docker is configured 
    - I use colima on macos (m2)
    - docker compose is installed

to expose to the public internet you can configure [a cloudflare tunnel](https://developers.cloudflare.com/cloudflare-one/connections/connect-networks/) that routes traffic to `http://webui:8080`.

create a .env file with [a cloudflare tunnel token(https://developers.cloudflare.com/cloudflare-one/connections/connect-networks/)]:

```sh
TUNNEL_TOKEN=your_token_here

```

bring up the docker compose stack:

```sh

docker compose up -d
```

the webui will be available locally at `http://localhost:3000`.

follow the logs:

```sh
docker compose logs -f
```

backup db:

```sh
colima ssh -- 'tar czf - /var/lib/docker/volumes/webui/_data' > webui-backup.tgz
```