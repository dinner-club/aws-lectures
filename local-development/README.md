# Developing AWS _Locally_

## Why Local?
One of the driving factors for using AWS is the cost savings associated with a well-tuned 'pay for what you actually use' app, but all it takes is one accidental recursive loop to spiral your AWS bill out of control [Insert link to scary articles when I find them again](#).

We feel safest when we can test things locally on our own machines, without having to pay for every request (or have our development efforts eat away at our precious free tier).

Luckily, there are a few really awesome tools we can use to test much of our everyday AWS applications right on our own machines, with rarely a need to make a full call to the AWS mothership.

## Requirements:
* An AWS account (free tier rocks)
* Ruby installed on your machine (I believe anything >= 2.4)
* [Docker desktop](https://www.docker.com/products/docker-desktop) installed
* Node (not sure which version)
* Python (at least 2.6.5)
  * [AWS-CLI](https://github.com/aws/aws-cli)

## Caveats:
Following the steps outlined in this readme will allow you write and test a lot of AWS functionality without calling their servers or actually deploying anything to the web. *However*, certain services cannot be run locally (translation services, image recognition, elastic search, etc.)

For the purpose of this document, the following can be safely developed without using your AWS credits:
* Local API Gateway
* Local Lambda Functions
* Local S3 storage (a little finicky, but still good to have in a pinch)
* Local DynamoDB

---

## AWS Setup

### Roles/Permissions
* Only permissions for what you need/use
* Narrower scope is better

### Cost Monitoring
* Set a limit and an alarm, just in case

### AWS-CLI
* Set user/permissions

---

## Documentation
One of the more annoying parts of learning AWS is navigating the different documentation sources. A quick search can turn up quite a few different pages (all from AWS) about the topic you are looking for, but rather than forcing you to sort through release articles, support docs, and topics in other languages, the following should help you to find the information you need quickly.

Consider this _The Hitchhiker's Guide to the Docs_.

### DON'T PANIC
_Always make sure you are logged into your AWS Dashboard when accessing the docs. Few things are as frustrating as finding the page you have been looking for, just to realize that you have to be signed in to see the information. ...and then losing the page after being distracted by the Dashboard after signing in._

* [AWS-CLI](https://docs.aws.amazon.com/cli/latest/index.html)
* SAM Local
  * [Specifications](https://github.com/awslabs/serverless-application-model/blob/master/versions/2016-10-31.md)
  * [Developer Guide](https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/serverless-sam-reference.html)
* [CloudFormation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/template-reference.html)
* Services
  * [DynamoDB](https://docs.aws.amazon.com/amazondynamodb/latest/APIReference/API_Operations_Amazon_DynamoDB.html)
* [JavaScript SDK](https://docs.aws.amazon.com/AWSJavaScriptSDK/latest/)

---

## Detailed Setup Instructions:

* [SAM-Local](./sam-local.md)
* [Local DynamoDB](./dynamo-db.md)
* [Local S3](./fakes3.md)

---

## Show Me the Code

### [HelloLocalAWS App](#notMadeYet)
