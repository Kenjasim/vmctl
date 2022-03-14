# vmctl

Simple bash script which can be used to control KVM virtual machines. The script utilises the virsh ClI alongside some other modules such as curl to store images

## Prerequisites

You must have KVM, libvirt and virsh installed. Also a bridged network interface.

## Usage

First install the shell script to the `usr/local/bin` directory

```bash
sudo cp vmctl /usr/local/bin
```

Then you can run some commands

```bash
vmctl create vm <name> --cpu 2 --ram 2048 --image ubuntu
vmctl create image <name> --url https://cloud-images.ubuntu.com/focal/current/focal-server-cloudimg-amd64.img
vmctl get vms
vmctl get images
vmctl delete vm <name>
vmctl delete image <name>
```
