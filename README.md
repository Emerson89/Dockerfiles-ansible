# Dockerfiles para acesso ansible

## Distros
- Centos 7
- Rocky 8
- Debian 10

## Imagem para uso de ansible em container já liberado acesso ssh
## Exemplo de uso

- DOCKER_CONTAINER_NAME="centos"
- DOCKER_IMAGE="emr001/centos7-emr"
- INIT=/usr/lib/systemd/systemd
- RUN_OPTS="--privileged --volume=/sys/fs/cgroup:/sys/fs/cgroup:ro" 

```
docker run -ti $RUN_OPTS --detach --volume="${PWD}":/etc/ansible/roles/role_under_test:ro -p 8080:80 --name $DOCKER_CONTAINER_NAME $DOCKER_IMAGE $INIT
```
# License
GLPv3