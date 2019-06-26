# packer-rtpengine

A [packer](https://www.packer.io/) template to build an AMI for rtpengine

## Installing 

```
$ git clone git@github.com:davehorton/packer-rtpengine.git
$ cd packer-rtpengine
$ git submodule update --init --recursive
$  packer build  \
-var 'aws_access_key=YOUR-ACCESS-KEY'  \
-var 'aws_secret_key=YOUR-SECRET-KEY' \
template.json
```

### variables
These variables can be specified on the `packer build` command line.  Defaults are listed below, where provided.
```
"aws_access_key": ""
```
Your aws access key.
```
"aws_secret_key": ""
```
Your aws secret key.

```
"region": "us-east-1"
```
The region to create the AMI in

```
"source_ami": "ami-024a64a6685d05041"
```
Source AMI to use.

```
ssh_username": "ubuntu"
```
ssh username to use when connecting to instance for provisioning

```
"ami_description": "EC2 AMI rtpengine Ubuntu 18.04"
```
AMI description.

```
"instance_type": "t2.medium"
```
EC2 Instance type to use when building the AMI.

```
"rtp_engine_version": "mr7.3.1.2"
```
rtpengine tag or branch to build

```
"cloud_provider": "aws"
```
Cloud provider the AMI will on.