<!-- TOC depthFrom:1 depthTo:6 withLinks:1 updateOnSave:1 orderedList:0 -->

		- [About](#about)
		- [Branch Names:](#branch-names)
			- [00/cleanStart](#00cleanstart)
			- [01/basicPlaybook](#01basicplaybook)
			- [02/shellAndDebugTasks](#02shellanddebugtasks)
			- [03/shellTaskNoChange](#03shelltasknochange)
			- [04/copyFile](#04copyfile)
			- [05/copyFileWithItems](#05copyfilewithitems)
			- [06/copyFileWithItemsAdv](#06copyfilewithitemsadv)
			- [07/templatesAndVars](#07templatesandvars)
			- [08/groupAndHostVarsLayout](#08groupandhostvarslayout)
			- [09/hostVarsOverwirte](#09hostvarsoverwirte)
			- [10/roles](#10roles)
			- [11/rolesTemplatesVSCopy](#11rolestemplatesvscopy)
			- [12/rolesTemplatesJinja2Syntax](#12rolestemplatesjinja2syntax)
			- [13/tags](#13tags)

<!-- /TOC -->

### About

This repo is meant to be used as part of a presentation to introduction people to Ansible.  Each branch represent a lesson, and the presenter should iterate through each branch describing each Ansible concept.  A minimum of 2 Linux systems is required for demonstrating concepts.  Talking points and links to documentation are provided in for each branch.

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
  * [shell module](http://docs.ansible.com/ansible/latest/shell_module.html)
  * [register](http://docs.ansible.com/ansible/latest/playbooks_conditionals.html#register-variables)
* Use the debug module to print out the variable contents in two different ways.
  * [debug module](http://docs.ansible.com/ansible/latest/debug_module.html)


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
* [template module](http://docs.ansible.com/ansible/latest/template_module.html)


#### 08/groupAndHostVarsLayout

Group/Host variables organizational layouts options.
* [splitting out host and group specific data](http://docs.ansible.com/ansible/latest/intro_inventory.html#splitting-out-host-and-group-specific-data)


#### 09/hostVarsOverwirte

Variable overwrite concept and Variable precedence
* [variable precedence](http://docs.ansible.com/ansible/latest/playbooks_variables.html#variable-precedence-where-should-i-put-a-variable)


#### 10/roles

Ansible roles and structure, demonstrating a role with 3 tasks
* [roles](http://docs.ansible.com/ansible/latest/playbooks_roles.html#roles)


#### 11/rolesTemplatesVSCopy

Choosing template over copy and how comment filter in templates makes it a better choice over copy
* [template comment filters](http://docs.ansible.com/ansible/latest/playbooks_filters.html#comment-filter)


#### 12/rolesTemplatesJinja2Syntax

JINJA2 syntax in combination with group_vars, demonstrating `for` loop and `if` conditional
* [jinja: for](http://jinja.pocoo.org/docs/2.9/templates/#for)
* [jinja: if](http://jinja.pocoo.org/docs/2.9/templates/#if)
* Group_vars/all:
  * [default/common](http://docs.ansible.com/ansible/latest/intro_inventory.html#default-groups)
  * [variable example](http://docs.ansible.com/ansible/latest/playbooks_variables.html#variable-examples)


#### 13/tags

Run specific parts of a playbook with tags.
* [tags](http://docs.ansible.com/ansible/latest/playbooks_tags.html#tags)
