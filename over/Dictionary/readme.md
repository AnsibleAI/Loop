sch: https://www.google.com/search?q=ansible+loop+dictionary

# Works:
https://stackoverflow.com/questions/42167747/how-to-loop-over-this-dictionary-in-ansible

## example:
Now Ansible allows this
```
- name: add several users
  user:
    name: "{{ item.name }}"
    state: present
    groups: "{{ item.groups }}"
  with_items:
    - { name: 'testuser1', groups: 'wheel' }
    - { name: 'testuser2', groups: 'root' }
```
