# Cozystack External Apps

Cozystack External Apps for the homelab

Read more about Cozystack at [cozystack.io](https://cozystack.io).

Reference documentation for Cozystack external-apps can be found at [cozystack.io/docs/applications/external](https://cozystack.io/docs/v1/applications/external/).

## Installation

```sh
kubectl apply -f https://raw.githubusercontent.com/BarryThePenguin/external-apps/main/init.yaml
```

Then watch the HelmReleases reconcile:

```sh
kubectl get hr -A
```

## Available Apps

| Package | Description |
| --- | --- |
| ghost | Managed Ghost blogging platform |
| mysql | Managed MySQL InnoDB Cluster |
| minecraft-server | Managed PaperMC Minecraft server with automatic updates and plugin management |
| minecraft-plugin | Managed Minecraft plugin with automatic version management |

Minecraft apps are powered by [minecraft-operator](https://github.com/lexfrei/minecraft-operator) via [cozylex](https://github.com/lexfrei/cozylex).
