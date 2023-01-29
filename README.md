# teslamate

![Version: 3.6.5](https://img.shields.io/badge/Version-3.6.5-informational?style=flat-square) ![AppVersion: v1.22.0](https://img.shields.io/badge/AppVersion-v1.22.0-informational?style=flat-square)

A self-hosted data logger for your Tesla 🚘

**This chart is not maintained by the upstream project and any issues with the chart should be raised [here](https://github.com/dkoshkin/teslamate-helm-chart/issues/new/choose)**

## Source Code

* <https://github.com/adriankumpf/teslamate>

## Requirements

TODO: add Grafana and PostgreSQL

## TL;DR

```console
helm repo add teslamate https://dkoshkin.github.com/teslamate-helm-chart
helm repo update
helm install teslamate teslamate/teslamate
```

## Installing the Chart

To install the chart with the release name `teslamate`

```console
helm install teslamate teslamate/teslamate
```

## Uninstalling the Chart

To uninstall the `teslamate` deployment

```console
helm uninstall teslamate
```

The command removes all the Kubernetes components associated with the chart **including persistent volumes** and deletes the release.

## Configuration

Read through the [values.yaml](./values.yaml) file. It has several commented out suggested values.

Specify each parameter using the `--set key=value[,key=value]` argument to `helm install`.

```console
helm install teslamate \
  --set env.TZ="America/New York" \
    teslamate/teslamate
```

Alternatively, a YAML file that specifies the values for the above parameters can be provided while installing the chart.

```console
helm install teslamate teslamate/teslamate -f values.yaml
```

## Custom configuration

N/A

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` |  |
| checkOrigin | bool | `false` |  |
| database.host | string | `nil` |  |
| database.user | string | `"teslamate"` |  |
| database.password | string | `"teslamate"` |  |
| database.database | string | `"teslamate"` |  |
| env | string | `{}` |  |
| envFromSecrets | object | `[]` |  |
| envFromConfigMaps | object | `[]` |  |
| fullnameOverride | string | `""` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"teslamate/teslamate"` |  |
| image.tag | string | `""` |  |
| ingress.annotations | object | `{}` |  |
| ingress.ingressClassName | string | `nil` |  |
| ingress.enabled | bool | `false` |  |
| ingress.hosts[0] | string | `"chart-example.local"` |  |
| ingress.path | string | `"/"` |  |
| ingress.pathType | string | `"ImplementationSpecific"` |  |
| ingress.tls | list | `[]` |  |
| locale | string | `"en"` |  |
| mqtt.enabled | bool | `false` |  |
| mqtt.host | string | `nil` |  |
| mqtt.password | string | `nil` |  |
| mqtt.tls | string | `nil` |  |
| mqtt.tlsAcceptInvalid | string | `nil` |  |
| mqtt.username | string | `nil` |  |
| nameOverride | string | `""` |  |
| nodeSelector | object | `{}` |  |
| probes.liveness.failureThreshold | int | `15` |  |
| probes.liveness.periodSeconds | int | `10` |  |
| probes.readiness.failureThreshold | int | `15` |  |
| probes.readiness.periodSeconds | int | `10` |  |
| probes.startup.failureThreshold | int | `30` |  |
| probes.startup.initialDelaySeconds | int | `15` |  |
| probes.startup.periodSeconds | int | `10` |  |
| remotePostgresql.enabled | bool | `false` |  |
| remotePostgresql.secretName | string | `""` |  |
| remotePostgresql.host | string | `nil` |  |
| remotePostgresql.user | string | `nil` |  |
| remotePostgresql.password | string | `nil` |  |
| remotePostgresql.database | string | `nil` |  |
| replicaCount | int | `1` |  |
| resources | object | `{}` |  |
| service.port | int | `4000` |  |
| service.type | string | `"ClusterIP"` |  |
| timeZone | string | `"UTC"` |  |
| tolerations | list | `[]` |  |
| virtualHost | string | `nil` |  |


## Support

- Open an [issue](https://github.com/dkoshkin/teslamate-helm-chart/issues/new/choose)
