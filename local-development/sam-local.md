# AWS SAM Local

## Installation
* [Homebrew](https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/serverless-sam-cli-install-mac.html) (Easiest)
* [pip](https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/serverless-sam-cli-install-additional.html#serverless-sam-cli-install-using-pip) (Requires you to manually update your PATH)

## Template Structure & CloudFormation
* [SAM Template Intro](https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/serverless-sam-template-basics.html)
* [SAM Specification](https://github.com/awslabs/serverless-application-model/blob/master/versions/2016-10-31.md)
* [CloudFormation Template Reference](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/template-reference.html)

## Initialize the default `helloWorld` project

Run:
```terminal
$ sam init
$ cd sam-app
$ sam build --use-container
```

## Run the `helloWorld` project

Run
```terminal
$ sam local start-api
```

## Debugging
If you aren't using VSCode and its incredible debugging features, now is a great time to start. AWS SAM provides a [quick guide for debugging Node and _Python_ Lambda functions in VSCode](https://github.com/awslabs/aws-sam-cli/blob/develop/docs/usage.md#debugging-applications).

Of course, you can always use the debugger of your choice for Lambdas written in JavaScript by exposing a port for debugging and pointing a debugger of your choice at the port.

```terminal
sam local start-api --debug-port 5858
```

For more information (like accessing logs), check the [SAM CLI Docs](https://github.com/awslabs/aws-sam-cli/blob/develop/docs/usage.md)


## Environment Variables
* [Using Environment Variables in a SAM Template](https://github.com/awslabs/aws-sam-cli/blob/develop/docs/advanced_usage.md#lambda-environment-variables)
* [Overriding Environment Variables using config files](https://github.com/awslabs/aws-sam-cli/blob/develop/docs/advanced_usage.md#environment-variable-file) (Useful for having a test/local config separate from your staging/prod configs)