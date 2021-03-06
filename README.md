### NFS JupyterHub Helm Chart

This repo was created to mitigate a very peculiar bug involving Rancher and kubeSpawner interpreting ints as strings. Consider it a default deployment for an NFS storage backed Jupyterhub, based on (v0.7.0) https://github.com/jupyterhub/helm-chart

The chart is on the gh-pages branch to allow Rancher to pull it as a catalog app https://github.com/Amir-Abushanab/jhub-nfs-chart/tree/gh-pages

The default values are set similar to those described here https://zero-to-jupyterhub.readthedocs.io/en/stable/amazon/efs_storage.html

The only other modification is that the network is set to `ClusterIP` - i.e you should add a separate ingress controller and make sure to generate and set a value for `proxy.secretToken`
