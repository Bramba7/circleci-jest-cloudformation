# CircleCi Jest and Aws CloudFormation project

### 10.2.0v

## Overview

## Prerequisities

In order to run this container you'll need docker installed.

- [Windows](https://docs.docker.com/windows/started)
- [OS X](https://docs.docker.com/mac/started/)
- [Linux](https://docs.docker.com/linux/started/)

Node.js installation.

- [Windows](https://phoenixnap.com/kb/install-node-js-npm-on-windows)
- [OS X](https://treehouse.github.io/installation-guides/mac/node-mac.html)
- [Linux](https://www.npmjs.com/get-npm/)

## Steps to Run

### AWS CloudFormation

To launch the entire stack and deploy on AWS, click on one of the **_Launch Stack_** links below or download the Master template and launch it locally.
You can launch this CloudFormation stack, using your account, in the following AWS Regions:

| AWS Region Code | Name                  | Launch                                                                                                                                                                                                                                |
| --------------- | --------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| us-east-1       | US East (N. Virginia) | [![launchstack](images/launchstack.png)](https://console.aws.amazon.com/cloudformation/home?region=us-east-1#/stacks/new?stackName=Trambo-ECS&templateURL=https://s3.amazonaws.com/assets.trambo.cloud/examples/ecs/master.yaml)      |
| us-east-2       | US East (Ohio)        | [![launchstack](images/launchstack.png)](https://console.aws.amazon.com/cloudformation/home?region=us-east-2#/stacks/new?stackName=Trambo-ECS&templateURL=https://s3.amazonaws.com/assets.trambo.cloud/examples/ecs/master.yaml)      |
| us-west-2       | US West (Oregon)      | [![launchstack](images/launchstack.png)](https://console.aws.amazon.com/cloudformation/home?region=us-west-2#/stacks/new?stackName=Trambo-ECS&templateURL=https://s3.amazonaws.com/assets.trambo.cloud/examples/ecs/master.yaml)      |
| eu-west-1       | EU (Ireland)          | [![launchstack](images/launchstack.png)](https://console.aws.amazon.com/cloudformation/home?region=eu-west-1#/stacks/new?stackName=Trambo-ECS&templateURL=https://s3.amazonaws.com/assets.trambo.cloud/examples/ecs/master.yaml)      |
| eu-central-1    | EU (Frankfurt)        | [![launchstack](images/launchstack.png)](https://console.aws.amazon.com/cloudformation/home?region=eu-central-1#/stacks/new?stackName=Trambo-ECS&templateURL=https://s3.amazonaws.com/assets.trambo.cloud/examples/ecs/master.yaml)   |
| ap-southeast-2  | AP (Sydney)           | [![launchstack](images/launchstack.png)](https://console.aws.amazon.com/cloudformation/home?region=ap-southeast-2#/stacks/new?stackName=Trambo-ECS&templateURL=https://s3.amazonaws.com/assets.trambo.cloud/examples/ecs/master.yaml) |

For more information about this cloudformation go to [TramboCloud/CF-ECS](https://github.com/TramboCloud/CF-ECS).

### Git Hub

Create a new repository on github and add these files in which CircleCi will run.

```shell
circleci-jest-cloudformation
├── .circleci/
│   └── config.yml           # → CircleCI 2.0 Config
├── images/
│   ├── launchstack.png      # → CloudFormation icon launch
│   ├──                      # →
│   └──                      # →
├── .gitignore               # → File that should not be push
├── Dockerfile               # → Uses to build a custom nginx container
├── README.md                # → Info about the github repo
├── index.html               # → Webpage that will be build on nginx container
├── package-lock.json        # → Jest parameters file
├── package.json             # → Test configuration
├── sketch.js                # → JavaScript function file
└── sketch.test.js           # → JavaScript test file

```

### CircleCI

Log in [CircleCI](https://circleci.com/) webpage with Github account.

### Environment variables in CircleCI

```
AWS_ACCESS_KEY_ID
AWS_REGION
AWS_SECRET_ACCESS_KEY
DOCKER_LOGIN
DOCKER_PASSWORD
ECS_CLUSTER_NAME
ECS_SERVICE
```

### NPM installation and Run

```
npm init
```

### Jest installation and config

```
npm install --save-dev jest
```

[Jest Config Info](https://jestjs.io/docs/en/getting-started.html)
