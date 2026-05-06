# WSO2 Developer Platform Sample REST API - Reading List

### Use the following configuration when creating this component in WSO2 Developer Platform:

- Build Preset: **Dockerfile**
- Dockerfile Path: `go-reading-list-rest-api/Dockerfile`
- Docker Context Path: `go-reading-list-rest-api`

The [endpoints.yaml](.choreo/endpoints.yaml) file contains the endpoint configurations that are used by the WSO2 Developer Platform to expose the service.

### Run the service locally

```shell
go run main.go
```

### Generate API definitions

Generated using Go annotations https://github.com/swaggo/swag

1. Download swag CLI tool by running: 
    ```shell
    go install github.com/swaggo/swag/cmd/swag@v1.8.11
    ```

2. Run the following command to generate the API definitions:
    ```shell
    swag fmt && swag init
    ```

### Service Configurations (optional)

Refer [config.go](internal/config/config.go) file for the available configurations.

For more information on how to configure a service in WSO2 Developer Platform, refer [Manage Configurations and Secrets](https://wso2.com/choreo/docs/deploy/devops/configs-and-secrets/) documentation.

#### Load initial data ( optional )

1. Set environment variable by navigating to WSO2 Developer Platform Deploy page `INIT_DATA_PATH=configs/initial_data.json`
2. Mount the file contents of `configs/initial_data.json` in the path specified in step 1.

See [initial_data.json](configs/initial_data.json) for a sample file.
