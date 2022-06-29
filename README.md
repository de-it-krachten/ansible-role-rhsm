[![CI](https://github.com/de-it-krachten/ansible-role-rhsm/workflows/CI/badge.svg?event=push)](https://github.com/de-it-krachten/ansible-role-rhsm/actions?query=workflow%3ACI)


# ansible-role-rhsm

Attach host to RHSM (Red Hat Subscription Management) 


## Platforms

Supported platforms

- Red Hat Enterprise Linux 7
- Red Hat Enterprise Linux 8
- Red Hat Enterprise Linux 9<sup>1</sup>

Note:
<sup>1</sup> : no automated testing is performed on these platforms

## Role Variables
### defaults/main.yml
<pre><code>
# RHSM activation key
rhsm_activationkey: "{{ lookup('env', 'RHSM_ACTIVATIONKEY') }}"

# RHSM organization id
rhsm_org_id: "{{ lookup('env', 'RHSM_ORG_ID') }}"
</pre></code>



## Example Playbook
### molecule/default/converge.yml
<pre><code>
- name: sample playbook for role 'rhsm'
  hosts: all
  vars:
  tasks:
    - name: Include role 'rhsm'
      include_role:
        name: rhsm
</pre></code>
