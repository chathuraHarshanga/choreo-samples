# Swagger Petstore Sample

This is the java project for a simplified version of the [pet store sample](https://github.com/swagger-api/swagger-petstore) hosted at https://petstore3.swagger.io.

## Repository File Structure

The below table gives a brief overview of the important files in the service.\
Note: The following file paths are relative to the path /java/pet-store/

| Filepath               | Description                                                                                                                                                  |
| ---------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| src/main               | The Java based service code.                                                                                                                                 |
| Dockerfile             | WSO2 Developer Platform uses the Dockerfile to build the container image of the application.                                                                                  |
| .choreo/endpoints.yaml | WSO2 Developer Platform-specific configuration that provides information about how the service is exposed.                                                                |
| openapi.yaml           | OpenAPI contract of the service. This is needed to publish our service as a managed API. This openapi.yaml file is referenced by the .choreo/endpoints.yaml. |

## Deploy Application

Please refer to the documentation under the [Develop a service with Dockerfile](https://wso2.com/choreo/docs/develop-components/develop-services/develop-a-service-with-docker/#step-1-create-a-service-component-from-a-dockerfile) section to learn how to deploy the application.

## Use the following build config when creating this component in WSO2 Developer Platform:

- Build Pack: **Dockerfile**
- Dockerfile Path: `java-docker-pet-store/Dockerfile`
- Docker Context Path: `java-docker-pet-store`

The [endpoints.yaml](.choreo/endpoints.yaml) file contains the endpoint configurations that are used by the WSO2 Developer Platform to expose the service.


### Execute the sample locally
Navigate to the Java application directory.
To run the server, run this command:

```
mvn package jetty:run
```

This will start Jetty embedded on port 8080.
