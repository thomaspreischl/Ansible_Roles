ctx-install-management-components
=========

This role can be used to install the Citrix backend components. With the exception of Storefront Server. This can be installed via the role ctx-install-storefront.


Requirements
------------

The server must be connected to the Active Directory and the file paths in the variable file should be correct.

Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in vars/ctx/xxx.yml (xxx = CTX Version Number). arameters to the role.
The settings, file paths for the installation files, etc. should all be set in the variable file for the particular version. In the playbook, the versions are to be passed along via the varfiles.

| Variable                | Required | Default | Choices                   | Comments                                 |
|-------------------------|----------|---------|---------------------------|------------------------------------------|
| destisofile             | yes      | false   |                           | example variable                         |
| srcisofile              | yes      | false   |                           | example variable                         |
| domain_admin            | yes      | false   |                           | example variable                         |
| domain_admin_password   | yes      | false   |                           | example variable                         |


Dependencies
------------

The dependencies, such as server roles, are listed in the respective playbook as an example or installed in the role accordingly. The dependent roles are also stored in the respective varfile.
In my homelab I installed some additional roles, because I like to have them installed on the controllers as well.

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