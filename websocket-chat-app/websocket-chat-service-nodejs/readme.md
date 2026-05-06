# WSO2 Developer Platform WebSocket Chat Application Example

Welcome to the WSO2 Developer Platform Nodejs Chat Application Example! This application is designed to help you get familiar with the platform and its features.

## Overview

This application is a webSocket service. It allows a clients create multiple persistent connections to the service and send and receive messages to an from the server.

## Repository File Structure

The below table gives a brief overview of the important files in the chat service.\
Note: The following file paths are relative to the path /websocket-chat-app/websocket-chat-service-nodejs

| Filepath                      | Description                                                                                   |
| ------------------------------| --------------------------------------------------------------------------------------------- |
| server.js                     | WebSocket service written in NodeJS.                                                          |
| .choreo/component-config.yaml | WSO2 Developer Platform-specific configuration that provides information about how the service is exposed. |

## Deploy Application

Please refer to the documentation under the [Develop a WebSocket API](https://wso2.com/choreo/docs/develop-components/develop-services/develop-a-nodejs-websocket-api/) section to learn how to deploy the application.

### Use the following configuration when creating this component in WSO2 Developer Platform:

- Build Pack: **NodeJS**
- Project Directory: `websocket-chat-app/websocket-chat-service-nodejs`

The [component-config.yaml](.choreo/component-config.yaml) file contains the endpoint configurations that are used by the WSO2 Developer Platform to expose the service.

### Test the service in WSO2 Developer Platform

Deploy the created component in WSO2 Developer Platform and navigate to the test page. In the WebSocket console, select the channel you want to test and click connect.

## Execute the Sample Locally

Navigate to the Chat Application directory

Run the service

```shell
npm start
```

Install the wscat client.

```shell
npm install -g wscat
```

To invoke the API, execute the following command:

```shell
wscat -c ws://localhost:8080/
```
Connect and pass messages as below,
```shell
{"type": "Connect", "username": "user1"}
{"type":"Data", "message":"Hello from user1"}
```
