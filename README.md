## Usage

[Helm](https://helm.sh) must be installed to use the charts.  Please refer to
Helm's [documentation](https://helm.sh/docs) to get started.

Once Helm has been set up correctly, add the repo as follows:

    helm repo add <alias> https://dapetri.github.io/helm-charts

If you had already added this repo earlier, run `helm repo update` to retrieve
the latest versions of the packages.  You can then run `helm search repo
<alias>` to see the charts.

To install the <chart-name> chart:

    helm install my-<chart-name> <alias>/<chart-name>

To uninstall the chart:

    helm delete my-<chart-name>

To upgrade the chart:

    helm repo update
    helm upgrade dafolio dapetri-charts/dafolio -n dafolio --version x.x.x

Workflow follows description from: https://helm.sh/docs/howto/chart_releaser_action/


Or do:

    helm upgrade -n dafolio -f charts/dafolio/values.yaml dafolio ./charts/dafolio 

