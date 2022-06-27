# Linux__virsh
How to manage VMs using CLI


## Creating VM

```
virt-install --name=ubuntu_test \
--vcpus=1 \
--memory=2048 \
--cdrom=/home/alisson-araujo/Downloads/ISOs/ubuntu-20.04.2-live-server-amd64.iso \
--disk size=5 \
--os-variant=ubuntu20.04
```

## Creating vm with two default NICs

```
virt-install --name=disk_size_test \
--vcpus=1 \
--memory=2048 \
--cdrom=/home/alisson-araujo/Downloads/ISOs/ubuntu-20.04.4-live-server-amd64.iso \
--disk size=7 \
--os-variant=ubuntu20.04 \
--network default \
--network default
```
## List VMs

virsh list --all

## Shutdown a VM

virsh shutdown <domain>

## Remove VM

virsh shutdown disk_size_test
virsh destroy disk_size_test
virsh undefine disk_size_test
rm -rf /var/lib/libvirt/images/disk_size_test.qcow2
  
_See more: virsh help or virt-install help_

## Managing hardware of created VM

https://www.thegeekstuff.com/2015/02/add-memory-cpu-disk-to-kvm-vm/
