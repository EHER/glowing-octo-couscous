## This is a Helm Chart Repository

### How to use it

Add [this url]() as your helm repo.
The syntax is `helm add <name> <url>`
```
helm repo add glowing-octo-couscous https://eher.com.br/glowing-octo-couscous/
```

One can use `helm repo list` to check it the repo was set properly:
```
helm repo list
```

Since the repo is set is possible to check the charts available with `helm search repo`:
```
helm search repo glowing-octo-couscous
```

Now that see the chart name `glowing-octo-couscous/kubephp` on the list let's go ahead and install it with `helm install`:
```
helm install --generate-name glowing-octo-couscous/kubephp
```

We can see the release status with `helm list`:
```
helm list
```

To release new versions from our chart repository, the repository information must be updated with `helm repo update` and then it is possible to upgrade your release with `helm upgrade <release name> <chart>`
```
helm repo update
helm upgrade kubephp-1643310091 glowing-octo-couscous/kubephp
```

The release should be upgraded if check again with `helm list`:

```
helm list
```

⎈Happy Helming!⎈

[index.yaml](index.yaml) gererated by [chart-releaser-action](https://github.com/helm/chart-releaser-action).
