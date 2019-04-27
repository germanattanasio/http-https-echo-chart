# http-https-echo-chart 🇦🇷

This helm chart deploys the [`http-https-echo`](https://github.com/mendhak/docker-http-https-echo) docker image to a kubernetes environment.

Kudos to [`mendhak`](https://github.com/mendhak) 🙌🙌🙌

## Installing the Chart

To install the chart with the release name `my-release` located in `<chart-directory>`:

```bash
helm install --name my-release <chart-directory>
```

This command deploys the chart with sane defaults.

A k8s service will be created with a ClusterIP configuration exposing two ports:
 * 8080 -> HTTP
 * 8443 -> HTTPs


## Verifying the Chart

See NOTES.txt associated with this chart for verification instructions

## Uninstalling the Chart

To uninstall/delete the `my-release` deployment:

```bash
helm delete my-release --purge
```

The command removes all the Kubernetes components associated with the chart and deletes the release.


## Configuration

| Parameter | Description | Default |
|-----------|-------------|---------|
| `image.repository` | Docker image repository | `mendhak/http-https-echo` |
| `image.tag` | Docker image tag | `latest`
| `image.pullPolicy` | Image pull policy | `IfNotPresent`
| `replicaCount` | Number of replicas | `1`
| `service.type` | Service type | `ClusterIP`
| `service.httpPort` | Service HTTP port number | `8080`
| `service.httpsPort` | Service HTTPS port number | `8443`


## LICENSE
MIT