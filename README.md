# AWS.ApiGatewayManagementApi()

This module adds the missing `ApiGatewayManagementApi()` constructor to `aws-sdk` [version 2.290.0](https://docs.aws.amazon.com/lambda/latest/dg/lambda-runtimes.html) included by current **AWS Lambda** default container so that the [Amazon API Gateway Management API](https://docs.aws.amazon.com/AWSJavaScriptSDK/latest/AWS/ApiGatewayManagementApi.html) service exposed without having to include the full [`aws-sdk`](https://www.npmjs.com/package/aws-sdk) module in the lambda build.

# How to use

```js
const ensureApiGatewayManagementApi = require('aws-apigatewaymanagementapi')
const AWS = require('aws-sdk');

ensureApiGatewayManagementApi(AWS) 

// Done, you can now use it, for example:
const managementApi = new AWS.ApiGatewayManagementApi({
  apiVersion: '2018-11-29',
});
```

# Forward compatible

If the local `aws-sdk` includes `ApiGatewayManagementApi` then this modules does nothing.
