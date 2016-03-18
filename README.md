# Stackity Stack Stack
This is a demo area for attempting to get an openstack installation up and running inside of vagrant, leveraging ansible and the ansible role ansible-puppet-executor

# Instructions
You will need to have a working copy of vagrant and vagrant-libvirt. For fedora machines this means

    sudo dnf install -y vagrant vagrant-libvirt

After checking out this repo run

    ansible-galaxy install -r requirements.yaml

To install some pre-requistite roles, then simply run

    vagrant up

To attempt to start the vagrant vm and provision it with ansible+puppet. Weather it's successful or fails, you can then go into the machine to check it out with

    vagrant ssh

If you want to rerun ansible on the machine (e.g. after changing the values in the inventory), simply run

    vagrant provision

# How it works
The ansible inventory (located in the inventory directory) has a raft of data in it which is directly fed into puppet via hiera. See the documentation for ansible-puppet-executor at https://github.com/ggillies/ansible-puppet-executor.git for details.
