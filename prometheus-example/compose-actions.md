

### Остановить и удалить
```shell
clear
podman compose down
podman ps -a
```

### Остановить и удалить + удалить volume с данными
```shell
podman compose down -v
podman ps -a
```

### Логи последние 100 строк за последний час
```shell
podman compose logs -f --tail 100 --since 1h 
```

### Запускаем 
```shell
clear
podman compose up -d
podman ps -a
```

### Метрики node-exporter
```shell
clear
curl --request GET -sL \
     --url 'http://localhost:9100/metrics'
```
```shell
# prometheus
open http://localhost:9090/targets
```
```shell
# grafana
# по умолчанию так и есть login: admin pass: admin
open http://localhost:3000
```

```shell
# allertmanager 
open http://localhost:9093
```

### Логи последние 100 строк за последний час
```shell
podman compose logs -f --tail 100 --since 1h 
```