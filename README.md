# AWS Summit Mexico

Serverless is a wonderful tool to manage serverless architectures but it also helps us to manage our CloudFormation templates in a better manner.

## Install

First, you need to create the initial CodePipeline and then all future changes will be deployed in automatic after a code change in the master branch.

You can use your own repository and token to test it.

```sh
serverless package --stage dev --verbose
serverless deploy --stage dev --verbose
```

## Uninstall

```sh
serverless remove --stage dev --verbose
```