# Observabilidade com Elastic
## Projeto do curso fullcycle developer

### Configurações

Crie a pasta elasticsearch_data na raíz do projeto
```sh
$ mkdir elasticsearch_data
``` 

Antes de executar o docker-compose up, crie a rede observability com o comando
```sh
$ docker network create observability
```
Na pasta /beats/metric execute o seguinte comando:

```sh
$ sudo chown root metricbeat.yml 
```
Caso ocorra o erro:
Bootstrap check failure [1] of [1]: max virtual memory areas vm.max_map_count [65530] is too low, increase to at least [262144]

Execute o comando:
```sh
sysctl -w vm.max_map_count=262144
```