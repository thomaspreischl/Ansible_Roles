ctx-install-management-components
=========

This role can be used to install the Citrix backend components. With the exception of Storefront Server. This can be installed via the role ctx-install-storefront.


Requirements
------------

The server must be connected to the Active Directory and the file paths in the variable file should be correct.

Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

| Variable                | Required | Default | Choices                   | Comments                                 |
|-------------------------|----------|---------|---------------------------|------------------------------------------|
| destisofile             | yes      | false   |                           | example variable                         |
| srcisofile              | yes      | false   |                           | example variable                         |
| domain_admin            | yes      | false   |                           | example variable                         |
| domain_admin_password   | yes      | false   |                           | example variable                         |


Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:


- hosts: ctxcontroller
  vars_files:
    - ./vars/ctx/2103.yml
  vars:
    components: CONTROLLER,DESKTOPSTUDIO,DESKTOPDIRECTOR,LICENSESERVER
  gather_facts: yes
  roles:
    - ctx-install-management-components


License
-------

See license.md

Author Information
------------------

https://www.thomaspreischl.de