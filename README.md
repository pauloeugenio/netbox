# Step By Step Netbox


# Step1:
```shell
git clone -b release https://github.com/netbox-community/netbox-docker.git
cd netbox-docker
tee docker-compose.override.yml <<EOF
version: '3.4'
services:
  netbox:
    ports:
      - 8000:8080
EOF
docker compose pull
docker compose up
```

A aplicação completa estará disponível após alguns minutos. Abra o URL http://0.0.0.0:8000/ em um navegador da web. Você deverá ver a página inicial do NetBox. Para criar o primeiro usuário administrador, execute este comando:

# Step2:
```docker compose exec netbox /opt/netbox/netbox/manage.py createsuperuser```





