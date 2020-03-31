```bash
docker service create --replicas 3 --name app -p 8080:8080 gcr.io/kubernetes-e2e-test-images/echoserver:2.2
```

```bash
docker service scale app=5                                                                                 
```

```bash
docker service rm app
```
