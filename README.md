ec24d - EC2 for dummies
=======================

A set of simple shell scripts for managing EC2 nodes.

Installation
------------

Download the following Amazon toolsets:

* EC2-Tools: http://aws.amazon.com/developertools/351
* ELB-Tools: http://aws.amazon.com/developertools/2536 

To install them, use something like this eg. in your profile:

```
export EC2_PRIVATE_KEY=~/.ec2/pk-YOURKEY.pem
export EC2_CERT=~/.ec2/cert-YOURKEY.pem

export EC2_HOME=$HOME/ec2-api-tools-1.5.0.1-2011.11.30/
export PATH=$PATH:$EC2_HOME/bin

export AWS_ELB_HOME=$HOME/ElasticLoadBalancing-1.0.17.0
export PATH=$PATH:$AWS_ELB_HOME/bin
```

Create a config file in your git root like the following:

```
APP=<your app name>
AMI=<your AMI, eg. ami-61555115>
TYPE=<instance type, eg. t1.micro>
KEYPAIR=<your keypair, eg. eu-pair>
REGION=<your region, eg. eu-west-1>
```

Usage
-----

`ec24d-start`
Creates a node, provisiones it and tags it to belong to the named application.

`ec24d-stop`
Terminates *all* nodes of the named application.

`ec24d-push`
Pushes the current git repo to the named app.

`ec24d-ssh [cmd]`
Peformes ssh on (one node of?) the named app. 

