# ansible-role-openscap

### Role to install the latest OpenSCAP.

The [Security Content Automation Protocol (SCAP)](http://scap.nist.gov/) is a U.S. standard maintained by the National Institute of Standards and Technology (NIST). SCAP provides a specification for system for vulnerability detetection and remediation.

SCAP supports the process of FISMA Compliance, and the [National Vulnerability Database (NVD)](http://nvd.nist.gov/) is the U.S. government content repository for SCAP.

[OpenSCAP](https://www.open-scap.org/) implements the standard and version 1.0.8 was awarded "NIST SCAP 1.2 certification" in 2014. It is a project created and supported by Red Hat and as such, has tradtionally been focused on the Red Hat (and CentOS) operating systems. But it is a flexible, open standard (if a bit obscure) and its use across other platforms and applications is growing.

Note that this role will install OpenSCAP version 1.2.x which has not yet received NIST certification.

### Quick start (testing with local vagrant instaces)

To make OpenSCAP easier/more manageable to use, see the [GovReady toolkit role](https://github.com/CivicActions/ansible-role-govready/).

### To install the latest openscap on your servers

Example `openscap-playbook.yml`:
```
- name: Install openscap on all servers
  hosts: servers
  roles:
    - { role: CivicActions.openscap, become: true }
```

Run command:
```
ansible-playbook -i inventory openscap-playbook.yml
```
