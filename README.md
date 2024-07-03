# Helm Chart for Filebrowser

This repository contains a Helm chart for deploying Filebrowser. It uses [**official filebrowser helm chart**](https://artifacthub.io/packages/helm/utkuozdemir/filebrowser) as a base and adds just the nginx ingress.


## Prerequisites

- Kubernetes 1.16+
- Helm 3.0+

## Installation

1. Add the Helm repository:
   `helm repo add filebrowser https://utkuozdemir.org/helm-charts`

2. Update the Helm repository:
   `helm repo update`

3. Install the Helm chart:
   `helm install my-filebrowser filebrowser/filebrowser`

## Uninstallation

To uninstall the Helm chart:
   `helm uninstall my-filebrowser`

## Configuration

The following table lists the configurable parameters of the Filebrowser chart and their default values.

| Parameter          | Description                       | Default           |
|--------------------|-----------------------------------|-------------------|
| `replicaCount`     | Number of replicas                | `1`               |
| `image.repository` | Image repository                  | `filebrowser/filebrowser` |
| `image.tag`        | Image tag                         | `latest`          |
| `image.pullPolicy` | Image pull policy                 | `IfNotPresent`    |
| `service.type`     | Service type                      | `ClusterIP`       |
| `service.port`     | Service port                      | `80`              |

Specify each parameter using the `--set key=value[,key=value]` argument to `helm install`. For example:

   `helm install my-filebrowser filebrowser/filebrowser --set replicaCount=2`

Alternatively, a YAML file that specifies the values for the parameters can be provided while installing the chart. For example:

   `helm install my-filebrowser filebrowser/filebrowser -f values.yaml`

## Values

Refer to the `values.yaml` file for the default values.