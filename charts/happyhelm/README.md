# Happy Helming Chart

* Echo Happy Helming!

## TL;DR;

```console
$ helm repo add govargo https://govargo.github.io/charts-repository
$ helm install govargo/happyhelm
```

## Installing the Chart

To install the chart with the release name `my-release`:

```console
$ helm install --name my-release govargo/happyhelm
```

## Uninstalling the Chart

To uninstall/delete the my-release deployment:

```console
$ helm delete my-release
```

The command removes all the Kubernetes components associated with the chart and deletes the release.


## Configuration

| Parameter                                 | Description                                   | Default                                                 |
|-------------------------------------------|-----------------------------------------------|---------------------------------------------------------|
| `replicaCount`                            | Number of pods                                | `1`                                                     |
| `image.repository`                        | Image repository                              | `govargo/happy-helming`                                 |
| `image.tag`                               | Image tag.                                    | `only-echo`                                             |
| `image.pullPolicy`                        | Image pull policy                             | `Always`                                                |
| `nameOverride`                            | Name Override                                 | ``                                                      |
| `fullnameOverride`                        | FullName Override                             | ``                                                      |
| `service.type`                            | Kubernetes service type                       | `LoadBalancer`                                          |
| `service.port`                            | Kubernetes port where service is exposed      | `80`                                                    |
| `livenessProbe`                           | Liveness Probe settings                       | `{ "tcpSocket": { "port": 8080 } }`                     |
| `readinessProbe`                          | Rediness Probe settings                       | `{ "httpGet": { "path": "/", "port": 8080 } }`          |
| `resources`                               | CPU/Memory resource requests/limits           | `{}`                                                    |
