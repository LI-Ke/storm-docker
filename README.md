# storm-docker

```
docker-compose up -d
```

```
docker exec -it waves_nimbus_1 /usr/local/redis/src/redis-server --daemonize yes
```

```
docker exec -it waves_nimbus_1 storm jar usr/local/waves-storm-0.2.0-SNAPSHOT.jar org.waves_rsp.storm.WavesTopology usr/local/test-topology.trig F-3f
```
