# Oracle JDK 7 (`oracle-jdk7`)
 
Master: [![Build Status](https://semaphoreci.com/api/v1/bas-ansible-roles-collection/oracle-jdk7/branches/master/badge.svg)](https://semaphoreci.com/bas-ansible-roles-collection/oracle-jdk7)
Develop: [![Build Status](https://semaphoreci.com/api/v1/bas-ansible-roles-collection/oracle-jdk7/branches/develop/badge.svg)](https://semaphoreci.com/bas-ansible-roles-collection/oracle-jdk7)
 
Installs Oracle Java Development Kit (JRE) 7
 
**Part of the BAS Ansible Role Collection (BARC)**
 
**This role uses version 0.2.0 of the BARC flavour of the BAS Base Project - Pristine**.
 
**NOTE:** By using this role you are agreeing to the terms of the Oracle license agreement for the Oracle Java JDK

## Overview
 
* Installs the Oracle Java JDK version 7
* Sets this JDK as the default JRE
 
## Quality Assurance
 
This role uses manual and automated testing to ensure its features work as advertised. 
See [here](tests/README.md) for more information.
 
## Dependencies
 
* None
 
More information on role dependencies is available in the 
[BARC General Documentation](https://antarctica.hackpad.com/BARC-Overview-and-Policies-SzcHzHvitkt#:h=Role-dependencies)
 
## Requirements
 
* None
 
More information on role requirements is available in the 
[BARC General Documentation](https://antarctica.hackpad.com/BARC-Overview-and-Policies-SzcHzHvitkt#:h=Role-requirements)
 
## Limitations
 
* None
 
More information on role limitations is available in the 
[BARC General Documentation](https://antarctica.hackpad.com/BARC-Overview-and-Policies-SzcHzHvitkt#:h=Role-limitations)
 
## Usage
 
### BARC Manifest
 
By default, BARC roles will record that they have been applied to a system, this is termed the BAS Manifest.
The specific local facts set for this role are:
 
* `ansible_local.barc_oracle_jdk7.general.role_applied` - (boolean) records whether a role has been applied
* `ansible_local.barc_oracle_jdk7.general.role_version` - (string) records the version of the role that was applied
 
Note: You **SHOULD** use this feature to determine whether this role has been applied to a system.
If you do not want these facts to be set by this role, you **MUST** skip the **BARC_SET_MANIFEST** tag.
 
More information is available in the 
[BARC General Documentation](https://antarctica.hackpad.com/BARC-Overview-and-Policies-SzcHzHvitkt#:h=Role-Manifest)
 
### Java version

This role will install Oracle Java 7 update 80 in both CentOS and Ubuntu.

### Default Java JRE

THis role will set the default system JRE to the Oracle Java 7 JDK by setting:

* Symbolic links to conventional locations in each respective operating system supported by this role
* Setting the value of the `JAVA_HOME` environment variable, available system wide

### Typical playbook
 
```yaml
---
 
- name: ...
  hosts: all
  become: yes
  vars: []
  roles:
    - bas-ansible-roles-collection.oracle-jdk7
```
 
### Tags
 
BARC roles use standardised tags to control which aspects of an environment are changed by roles.
Tasks in this role will 'tag' themselves with these tags as appropriate, typically in `tasks/main.yml`.
 
More information is available in the
[BARC General Documentation](https://antarctica.hackpad.com/BARC-Overview-and-Policies-SzcHzHvitkt#:h=Appendix-B---BARC-Standardised)
 
### Variables
 
#### *oracle_jdk7_barc_role_name*
 
* **MUST NOT** be specified
* Specifies the name of this role within the BAS Ansible Roles Collection (BARC) used for setting local facts
* See the *BARC roles manifest* section for more information
* Example: `oracle_jdk7` 
 
#### *oracle_jdk7_barc_role_version*
 
* **MUST NOT** be specified
* Specifies the name of this role within the BAS Ansible Roles Collection (BARC) used for setting local facts
* See the *BARC roles manifest* section for more information
* Example: `2.0.0` 
 
## Developing
 
### Issue tracking
 
Issues, bugs, improvements, questions, suggestions and other tasks related to this package are managed through the 
[BAS Ansible Roles Collection](https://jira.ceh.ac.uk/projects/BARC) (BARC) project on Jira.
 
This service is currently only available to BAS or NERC staff, although external collaborators can be added on request.
See our contributing policy for more information.
 
More information is also available in the
[BARC General Documentation](https://antarctica.hackpad.com/BARC-Overview-and-Policies-SzcHzHvitkt#:h=Issue-Tracking)
 
### Source code
 
All changes should be committed, via pull request, to the canonical repository:
 
`ssh://git@stash.ceh.ac.uk:7999/barc/ROLE-NAME.git` 
 
A read-only mirror of this repository is maintained on GitHub:
 
`git@github.com:bas-ansible-roles-collection/ROLE-NAME.git`
 
More information is available in the
[BARC General Documentation](https://antarctica.hackpad.com/BARC-Overview-and-Policies-SzcHzHvitkt#:h=Source-Code)
 
### Contributing policy
 
This project welcomes contributions, see `CONTRIBUTING.md` for our general policy.
 
### Release procedure
 
The general release procedure for BARC roles is available in the
[BARC General Documentation](https://antarctica.hackpad.com/BARC-Overview-and-Policies-SzcHzHvitkt#:h=Release-procedures)
 
## Licence
 
Copyright 2016 NERC BAS.
 
Unless stated otherwise, all documentation is licensed under the Open Government License - version 3.
All code is licensed under the MIT license.
 
Copies of these licenses are included within this project.
