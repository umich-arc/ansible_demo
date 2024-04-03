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


#### 02/shellAndDebugTasks

Use shell module, how to register(store) output from the shell
command into a variable, and use debug module to print the values to the screen.

* Run a shell command to gather disk usage and store results in a variable. Read:
  * [shell module](https://docs.ansible.com/ansible/latest/collections/ansible/builtin/shell_module.html#ansible-collections-ansible-builtin-shell-module)
  * [register](http://docs.ansible.com/ansible/latest/playbooks_conditionals.html#register-variables)
* Use the debug module to print out the variable contents in two different ways.
  * [debug module](https://docs.ansible.com/ansible/latest/collections/ansible/builtin/debug_module.html#ansible-collections-ansible-builtin-debug-module)


#### 03/shellTaskNoChange

Shell commands will always report a change even if you are just doing a directory
listing.  Behavior can be overwritten with changed_when property.
* [overriding the changed result](http://docs.ansible.com/ansible/latest/playbooks_error_handling.html#overriding-the-changed-result)


#### 04/copyFile

Playbook to copy a file demonstrating rename from src to dest and backup options.
* [copy module](http://docs.ansible.com/ansible/latest/copy_module.html)


#### 05/copyFileWithItems

Copy more than one file in a task, demonstrating the with_items feature of Ansible
* [standard loop](http://docs.ansible.com/ansible/latest/playbooks_loops.html#standard-loops)


#### 06/copyFileWithItemsAdv

A continuation of standard loops (with_items) using list of hashes.
* [standard loops](http://docs.ansible.com/ansible/latest/playbooks_loops.html#standard-loops)


#### 07/templatesAndVars

Concept of group and host variables in reference to the inventory, and how to use the template module
to render templates as files on destination system.
* [host variables](http://docs.ansible.com/ansible/latest/intro_inventory.html#host-variables)
* [group variables](http://docs.ansible.com/ansible/latest/intro_inventory.html#group-variables)
* [template module](https://docs.ansible.com/ansible/latest/collections/ansible/builtin/template_module.html#ansible-collections-ansible-builtin-template-module)


#### 08/groupAndHostVarsLayout

Group/Host variables organizational layouts options.
* [splitting out host and group specific data](http://docs.ansible.com/ansible/latest/intro_inventory.html#splitting-out-host-and-group-specific-data)


#### 09/hostVarsOverwirte

Variable overwrite concept and Variable precedence
* [variable precedence](http://docs.ansible.com/ansible/latest/playbooks_variables.html#variable-precedence-where-should-i-put-a-variable)
