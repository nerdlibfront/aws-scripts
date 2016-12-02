Some small AWS scripts
======================

These are some scripts that i use quite often in conjunction with AWS.
They all assume that you launch a Amazon Linux AMI.

make-instance-docker-ready.sh
-----------------------------

This script does the security updates, installs docker and sets the needed privileges for the ec2-user.

Usage:

Add the following code to your UserData when creating a new instance.
Be aware that this executes just what i have pushed to github, so if you don't trust me, fork this script before you use it!

	#!/bin/bash
	bash <(curl -s https://raw.githubusercontent.com/nerdlibfront/aws-scripts/master/make-instance-docker-ready.sh)

To check if it worked, ssh into your instance and run `docker info`. If this echos out data of the docker daemon your instance is ready to use docker.

