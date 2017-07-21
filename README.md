### Branch Names:

#### 00/cleanStart

Clean install directory layout.
* Look at the ansible.cfg file. The file is well documented but you can get more
details at the [Ansible Configuration file link](http://docs.ansible.com/ansible/latest/intro_configuration.html)
* Take a look at the hosts file.  This is where you can define your inventory,
some examples are provided.  For more details see the [Ansible Inventory documentation](http://docs.ansible.com/ansible/latest/intro_inventory.html)


#### 01/basicPlaybook

Populate the inventory file and simple playbook.

* Inventory, demonstrating the concept of groups, group of groups, and aliases.
Read more [Ansible Inventory documentation](http://docs.ansible.com/ansible/latest/intro_inventory.html)
* Simple playbook that will check to make sure it can talk to each host via ssh.
Read:
   * [Playbooks](http://docs.ansible.com/ansible/latest/playbooks.html)
   * [hosts](http://docs.ansible.com/ansible/latest/playbooks_intro.html#hosts-and-users)
   * [tasks](http://docs.ansible.com/ansible/latest/playbooks_intro.html#tasks-list)
   * [ping module](http://docs.ansible.com/ansible/latest/ping_module.html)
   * [Executing a Playbook](http://docs.ansible.com/ansible/latest/playbooks_intro.html#executing-a-playbook)
