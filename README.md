# ansible-nfs
Ansible playbook to install and configure NFS server

Install / configure NFS:

(WARNING: This will wipe all data on the devices/partitions you have set in the group_vars!)

`ansible-playbook -i hosts nfs.yml`

Remove NFS:

(This will not wipe data, just unmount the devices/partitions)

`ansible-playbook -i hosts nfs.yml -e "{unmount: true}"`

If you get errors saying a device is busy, trying rebooting the machine and running the playbook again
