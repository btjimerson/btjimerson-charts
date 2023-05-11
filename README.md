## Usage

[Helm](https://helm.sh) must be installed to use the charts.  Please refer to Helm's [documentation](https://helm.sh/docs) to get started.

Once Helm has been set up correctly, add the repo as follows:

```bash
helm repo add btjimerson https://btjimerson.github.io/btjimerson-charts
helm repo update
```

If you had already added this repo earlier, run `helm repo update` to retrieve the latest versions of the packages.  You can then run `helm search repo btjimerson` to see the charts.

To install the ecommerce-demo chart, first create a file called values.yaml and override certain values. At a minimum, these values should be set:

 * `global.activeProfile`
 * `payments.stripeApiKey`

 Then you can install the chart:

```bash
helm install --values values.yaml my-ecommerce-demo btjimerson/ecommerce-demo
```

To uninstall the chart:

```bash
helm uninstall delete my-ecommerce-demo
```
