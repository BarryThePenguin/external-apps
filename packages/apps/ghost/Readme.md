# Managed Ghost Service

This chart installs a Ghost blog.

Installation notes:

- Default values are in `values.yaml`.
- To enable ingress, set `ingress.enabled: true` and configure hosts.

This chart is placed in `packages/apps/ghost` so Cozystack can surface it in the dashboard catalog.

For customization, update `values.yaml` or provide overrides when installing the chart.

## Parameters

### Common Parameters

| Name           | Description                          | Type     | Value        |
| -------------- | ------------------------------------ | -------- | ------------ |
| `storageClass` | StorageClass used to store the data. | `string` | `replicated` |


### Application-specific Parameters

| Name                           | Description                                                                                | Type     | Value                     |
| ------------------------------ | ------------------------------------------------------------------------------------------ | -------- | ------------------------- |
| `replicas`                     | Number of Ghost replicas.                                                                  | `int`    | `1`                       |
| `host`                         | Hostname for external access to Ghost (defaults to 'ghost' subdomain for the tenant host). | `string` | `""`                      |
| `admin`                        | Configuration for the Ghost admin interface.                                               | `object` | `{}`                      |
| `admin.url`                    | The URL for the Ghost admin interface (e.g., https://myblog.com/ghost).                    | `string` | `""`                      |
| `database`                     | Configuration for the database connection.                                                 | `object` | `{}`                      |
| `database.client`              | The database client type                                                                   | `string` | `mysql`                   |
| `database.connection`          | The database connection details.                                                           | `object` | `{}`                      |
| `database.connection.host`     | The database host address.                                                                 | `string` | `""`                      |
| `database.connection.user`     | The database username.                                                                     | `string` | `ghost`                   |
| `database.connection.password` | The database password.                                                                     | `string` | `""`                      |
| `database.connection.database` | The name of the database to connect to.                                                    | `string` | `ghost`                   |
| `tinybird`                     | Configuration for integrating with Tinybird analytics.                                     | `object` | `{}`                      |
| `tinybird.trackerEndpoint`     | The endpoint URL for sending tracking data to Tinybird.                                    | `string` | `""`                      |
| `tinybird.adminToken`          | The admin token for authenticating with Tinybird.                                          | `string` | `""`                      |
| `tinybird.workspaceId`         | The Tinybird workspace ID where data will be sent.                                         | `string` | `""`                      |
| `tinybird.trackerDatasource`   | The Tinybird datasource name for tracking data                                             | `string` | `analytics_events`        |
| `tinybird.statsEndpoint`       | The base URL for Tinybird API endpoints.                                                   | `string` | `https://api.tinybird.co` |

