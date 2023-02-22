# Alpharetta Use

Call from here: 
helm upgrade prometheus-stack ./charts/kube-prometheus-stack/ -f ./charts/kube-prometheus-stack/local-vaules.yaml -n prometheus --kube-context alpharetta

expose grafana port: 
kubectl expose service prometheus-stack-grafana -n prometheus --type=NodePort --target-port=3000 --name=grafana-ext

Check port number with `kubectl get services -n prometheus`
open port in browser


# Prometheus Community Kubernetes Helm Charts

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0) ![Release Charts](https://github.com/prometheus-community/helm-charts/workflows/Release%20Charts/badge.svg?branch=main) [![Releases downloads](https://img.shields.io/github/downloads/prometheus-community/helm-charts/total.svg)](https://github.com/prometheus-community/helm-charts/releases)

This functionality is in beta and is subject to change. The code is provided as-is with no warranties. Beta features are not subject to the support SLA of official GA features.

## Usage

[Helm](https://helm.sh) must be installed to use the charts.
Please refer to Helm's [documentation](https://helm.sh/docs/) to get started.

Once Helm is set up properly, add the repo as follows:

```console
helm repo add prometheus-community https://prometheus-community.github.io/helm-charts
```

You can then run `helm search repo prometheus-community` to see the charts.

## Contributing

The source code of all [Prometheus](https://prometheus.io) community [Helm](https://helm.sh) charts can be found on Github: <https://github.com/prometheus-community/helm-charts/>

<!-- Keep full URL links to repo files because this README syncs from main to gh-pages.  -->
We'd love to have you contribute! Please refer to our [contribution guidelines](https://github.com/prometheus-community/helm-charts/blob/main/CONTRIBUTING.md) for details.

## License

<!-- Keep full URL links to repo files because this README syncs from main to gh-pages.  -->
[Apache 2.0 License](https://github.com/prometheus-community/helm-charts/blob/main/LICENSE).

## Helm charts build status

![Release Charts](https://github.com/prometheus-community/helm-charts/workflows/Release%20Charts/badge.svg?branch=main)
