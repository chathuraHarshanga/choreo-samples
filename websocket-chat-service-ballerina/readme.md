# WSO2 Developer Platform Chat Service Example

Welcome to the WSO2 Developer Platform Chat Service Example! This application is designed to help you get familiar with the platform and its features.

## Overview

This application is a webSocket service. It allows a clients create multiple persistent connections to the service and send and recieve messages to an from the server.

## Repository File Structure

The below table gives a brief overview of the important files in the chat service.\
Note: The following file paths are relative to the path /ballerina/readling-list

| Filepath               | Description                                                                                   |
| ---------------------- | --------------------------------------------------------------------------------------------- |
| main.bal               | WebSocket service code written in the Ballerina language.                                       |
| Ballerina.toml         | Ballerina configuration file.                                                                 |
| .choreo/endpoints.yaml | WSO2 Developer Platform-specific configuration that provides information about how the service is exposed. |

## Deploy Application

Please refer to the documentation under the [Develop a Ballerina WebSocket API](https://wso2.com/choreo/docs/develop-components/develop-services/develop-a-ballerina-websocket-api/) section to learn how to deploy the application.

### Use the following configuration when creating this component in WSO2 Developer Platform:

- Build Pack: **Ballerina**
- Project Directory: `chat-service-websocket`

The [endpoints.yaml](.choreo/endpoints.yaml) file contains the endpoint configurations that are used by the WSO2 Developer Platform to expose the service.

### Test the service in WSO2 Developer Platform

Deploy the created component in WSO2 Developer Platform and navigate to the test page. In the WebSocket console, select the channel you want to test and click connect.

## Execute the Sample Locally

Navigate to the Ballerina WebSocket application directory

Run the service

```shell
bal run
```

Install the wscat client.

```shell
npm install -g wscat
```

To invoke the API, execute the following command:

```shell
wscat -c http://localhost:9090/chat'
```
