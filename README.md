# convert_to_nac

A role that takes a downloaded backup of ACI Fabric configuration, and generates a Nexus-as-Code formatted output that can then be used to manage a fabric using Nexus-as-Code IAC.

## Requirements

jinja2 and jmespath

## Role Variables

Create an inventory and place .json backup file in `inventory/host_vars/*`.  I created directories names after each fabric's APIC Node 1 hostname, your mileage may vary.  This json file will be picked up and processed by various tasks in the role.

## Dependencies

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).

## Example JMESPATH Queries

### Get list of Access Port Profiles

`polUni.children[].infraInfra.children[].infraAccPortP.attributes.name`
