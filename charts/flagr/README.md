
# flagr

A Helm chart for Flagr, a feature flagging and configuration management platform.

![Version: 1.17.0-alpha](https://img.shields.io/badge/Version-1.17.0--alpha-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 1.17.0](https://img.shields.io/badge/AppVersion-1.17.0-informational?style=flat-square)

## Installing the Chart

To install the chart with the release name `flagr`:

```bash
helm repo add flagr https://ericbsantana.github.io/flagr-helm-chart
```
```bash
helm install flagr flagr/flagr --devel
```

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| ericbsantana | <bitencourteric@hotmail.com> | <https://ericbsantana.com> |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` |  |
| autoscaling.enabled | bool | `false` | This enables autoscaling, see https://kubernetes.io/docs/concepts/workloads/autoscaling/ |
| autoscaling.maxReplicas | int | `100` | This sets the maximum number of replicas |
| autoscaling.minReplicas | int | `1` | This sets the minimum number of replicas |
| autoscaling.targetCPUUtilizationPercentage | int | `80` | This sets the target CPU utilization percentage |
| extraEnvs | list | `[]` | This is for setting additional environment variables, check Flagr environment variables here: https://openflagr.github.io/flagr/#/flagr_env |
| fullnameOverride | string | `""` |  |
| image.pullPolicy | string | `"IfNotPresent"` | This sets the pull policy for images. |
| image.repository | string | `"ghcr.io/openflagr/flagr"` | This sets the repository for the image |
| image.tag | string | `"1.1.17"` | Overrides the image tag whose default is the chart appVersion. |
| imagePullSecrets | list | `[]` | This is for the secretes for pulling an image from a private repository more information can be found here: https://kubernetes.io/docs/tasks/configure-pod-container/pull-image-private-registry/ |
| ingress | object | `{"annotations":{},"className":"","enabled":false,"hosts":[{"host":"chart-example.local","paths":[{"path":"/","pathType":"ImplementationSpecific"}]}],"tls":[]}` | This block is for setting up the ingress for more information can be found here: https://kubernetes.io/docs/concepts/services-networking/ingress/ |
| livenessProbe | object | `{"httpGet":{"path":"/api/v1/health","port":"http"}}` | This is to setup the liveness and readiness probes more information can be found here: https://kubernetes.io/docs/tasks/configure-pod-container/configure-liveness-readiness-startup-probes/ |
| nameOverride | string | `""` | This is to override the chart name. |
| nodeSelector | object | `{}` |  |
| podAnnotations | object | `{}` | For more information checkout: https://kubernetes.io/docs/concepts/overview/working-with-objects/annotations/ |
| podLabels | object | `{}` | For more information checkout: https://kubernetes.io/docs/concepts/overview/working-with-objects/labels/ |
| podSecurityContext | object | `{}` |  |
| readinessProbe.httpGet.path | string | `"/api/v1/health"` |  |
| readinessProbe.httpGet.port | string | `"http"` |  |
| replicaCount | int | `1` | This will set the replicaset count more information can be found here: https://kubernetes.io/docs/concepts/workloads/controllers/replicaset/ |
| resources | object | `{}` |  |
| securityContext | object | `{}` |  |
| service | object | `{"port":18000,"type":"ClusterIP"}` | This is for setting up a service more information can be found here: https://kubernetes.io/docs/concepts/services-networking/service/ |
| service.port | int | `18000` | This sets the ports more information can be found here: https://kubernetes.io/docs/concepts/services-networking/service/#field-spec-ports |
| service.type | string | `"ClusterIP"` | This sets the service type more information can be found here: https://kubernetes.io/docs/concepts/services-networking/service/#publishing-services-service-types |
| serviceAccount.annotations | object | `{}` | Annotations to add to the service account |
| serviceAccount.automount | bool | `true` | Automatically mount a ServiceAccount's API credentials? |
| serviceAccount.create | bool | `true` | Specifies whether a service account should be created |
| serviceAccount.name | string | `""` | If not set and create is true, a name is generated using the fullname template |
| tolerations | list | `[]` |  |
| volumeMounts | list | `[]` | Additional volumeMounts on the output Deployment definition. |
| volumes | list | `[]` | Additional volumes on the output Deployment definition. |

