# storm-docker

```
docker-compose up -d
```
containers' IPs:
zookeeper :        172.17.0.2
kafka :            172.17.0.3
tomcat(sesame) :   172.17.0.4
storm-nimbus :     172.17.0.5
storm-supervisor : 172.17.0.6
storm-ui :         172.17.0.7

start redis
```
docker exec -it waves_nimbus_1 /usr/local/redis/src/redis-server --daemonize yes
```
execute the application on storm
```
docker exec -it waves_nimbus_1 storm jar usr/local/waves-storm-0.2.0-SNAPSHOT.jar org.waves_rsp.storm.WavesTopology usr/local/test-topology.trig F-3f
```
visit sesame from storm nimbus
```
docker exec -it waves_nimbus_1 curl http://172.17.0.4:8080

docker exec -it waves_nimbus_1 curl http://172.17.0.4:8080/openrdf-workbench/repositories/waves/export
```
sesame page: http://localhost:8080/openrdf-workbench
storm UI: http://localhost:49080

