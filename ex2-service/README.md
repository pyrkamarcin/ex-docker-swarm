```bash
docker service create --replicas 3 --name app -p 8080:8080 gcr.io/kubernetes-e2e-test-images/echoserver:2.2
```

```bash
docker service update --publish-add 8080:8080 app
```

```bash
docker service update --limit-cpu 0.5 --limit-memory 209715200 app
```

```bash
docker service rollback app
```

```bash
docker service rm app
```