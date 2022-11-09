# Unitest
Helm chart of Prometheus Grafana and Blackbox exporter

Blackbox exporter target - https://www.google.com

## Usage

[Helm](https://helm.sh) must be installed to use the charts.
Please refer to Helm's [documentation](https://helm.sh/docs/) to get started.


Once Helm is set up properly, add the repo with the name `unitest` as follows:

```console
helm repo add unitest https://dfy24.github.io/unitest/
helm repo update
```

In values.yaml default namespace is `unitest` so to install the chart, first you need to create a namespace `unitest`:

```console
kubectl create namespace unitest
kubectl config set-context --current --namespace=unitest
```

To install the chart with the release name `unitest-release`:

```console
helm install unitest-release unitest/prometheus-grafana-blackbox-chart
```

## Grafana UI
Grafana UI for testing purposes is accessible via `30003 port` because of NodePort Service.

User: admin <br />
Password: unitest123
