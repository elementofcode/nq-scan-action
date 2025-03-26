# NeonQuery Scan action

Scans your repository with the NeonQuery client and uploads the results to the NeonQuery platform.

## Usage

```yaml
steps:
  - uses: actions/checkout@v4
  - uses: elementofcode/nq-scan-action@v1
    with:
      client_id: ${{ secrets.NEONQUERY_CLIENT_ID }}
      client_secret: ${{ secrets.NEONQUERY_CLIENT_SECRET }}
      config: ./nq.toml
      project: my-project
```

## Inputs

| Name            | Description                                    | Required | Default     |
| --------------- | ---------------------------------------------- | -------- | ----------- |
| `client_id`     | The NeonQuery API client id.                   | true     |             |
| `client_secret` | The NeonQuery API client secret.               | true     |             |
| `config`        | The path to the NeonQuery configuration file.  | false    | `./nq.toml` |
| `project`       | The name of the project you want to scan name. | true     |             |
