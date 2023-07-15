## Instalar docker

```bash
     curl -fsSL https://get.docker.com -o get-docker.sh && bash  get-docker.sh
     sudo usermod -aG docker $USER
```

## Criar volume para o portainer

```bash
    docker volume create portainer_data
```

## Instalar traefik e portainer

```bash
    docker stack deploy -c portainer-compose.yml portainer
    docker stack deploy -c traefik-compose.yml portainer
```

## Habilitar os hosts

```bash
    cat hosts >> /etc/hosts
```
