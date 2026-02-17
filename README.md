# Packer tutorial

## Steps
- Clone the repository
```
git clone git@github.com-work:mohamed-hashicorp/packer_tutorial.git
```
- Change directory
```
cd packer_tutorial
```
- Run the following commands
```
packer init .
packer fmt .
packer validate .
```
- Build the image

```
packer build aws-ubuntu.pkr.hcl
learn-packer.amazon-ebs.ubuntu: output will be in this color.
==> learn-packer.amazon-ebs.ubuntu: Prevalidating any provided VPC information
==> learn-packer.amazon-ebs.ubuntu: Prevalidating AMI Name: learn-packer-linux-aws
==> learn-packer.amazon-ebs.ubuntu: Found Image ID: ami-055c254ebd87b4dba
==> learn-packer.amazon-ebs.ubuntu: Creating temporary keypair: packer_699427da-a6a2-dff7-42d6-d803a55822a0
==> learn-packer.amazon-ebs.ubuntu: Creating temporary security group for this instance: packer_699427dc-2e0f-b685-8d88-85167e7cbd88
==> learn-packer.amazon-ebs.ubuntu: Authorizing access to port 22 from [0.0.0.0/0] in the temporary security groups...
==> learn-packer.amazon-ebs.ubuntu: Launching a source AWS instance...
==> learn-packer.amazon-ebs.ubuntu: Instance ID: i-0d9ecc3e5cda7b759
==> learn-packer.amazon-ebs.ubuntu: Waiting for instance (i-0d9ecc3e5cda7b759) to become ready...
==> learn-packer.amazon-ebs.ubuntu: Using SSH communicator to connect: 16.145.222.242
==> learn-packer.amazon-ebs.ubuntu: Waiting for SSH to become available...
==> learn-packer.amazon-ebs.ubuntu: Connected to SSH!
==> learn-packer.amazon-ebs.ubuntu: Stopping the source instance...
==> learn-packer.amazon-ebs.ubuntu: Stopping instance
==> learn-packer.amazon-ebs.ubuntu: Waiting for the instance to stop...
==> learn-packer.amazon-ebs.ubuntu: Creating AMI learn-packer-linux-aws from instance i-0d9ecc3e5cda7b759
==> learn-packer.amazon-ebs.ubuntu: Attaching run tags to AMI...
==> learn-packer.amazon-ebs.ubuntu: AMI: ami-04260bc8b4408d6fe
==> learn-packer.amazon-ebs.ubuntu: Waiting for AMI to become ready...
==> learn-packer.amazon-ebs.ubuntu: Skipping Enable AMI deprecation...
==> learn-packer.amazon-ebs.ubuntu: Skipping Enable AMI deregistration protection...
==> learn-packer.amazon-ebs.ubuntu: Terminating the source AWS instance...
==> learn-packer.amazon-ebs.ubuntu: Cleaning up any extra volumes...
==> learn-packer.amazon-ebs.ubuntu: No volumes to clean up, skipping
==> learn-packer.amazon-ebs.ubuntu: Deleting temporary security group...
==> learn-packer.amazon-ebs.ubuntu: Deleting temporary keypair...
Build 'learn-packer.amazon-ebs.ubuntu' finished after 4 minutes 14 seconds.

==> Wait completed after 4 minutes 14 seconds

==> Builds finished. The artifacts of successful builds are:
--> learn-packer.amazon-ebs.ubuntu: AMIs were created:
us-west-2: ami-04260bc8b4408d6fe
```