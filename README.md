# AWS Summit Mexico

Serverless is a wonderful tool to manage serverless architectures but it also helps us to manage our CloudFormation templates in a better manner.

## Requirements

```
serverless
cfn-lint (optional)
```

## Validate template

```sh
serverless package --stage dev --verbose
cfn-lint .serverless/cloudformation-template-update-stack.json
```

## Install

Create the initial CodePipeline and then all future changes will be deployed in automatic after a code change in the master branch. You can use your own repository and token to test it.

```sh
serverless deploy --stage dev --verbose
```

## Uninstall

Clean up all objects form artifacts buckets, update `buildspec.yaml` to remove serverless services and then you can save remove the initial pipeline

```sh
serverless remove --stage dev --verbose
```