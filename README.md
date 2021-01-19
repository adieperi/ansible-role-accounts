# ansible-role-accounts
Manage local accounts

```yaml
---
- name: Setup root authorized keys and remove administrator account
      include_role:
        name: ansible-role-accounts
      vars:
        accounts:
          remove:
            user:
              - administrator
        authorizedKeys:
          add:
            user: root
            sshKeys: 
               - https://github.com/adieperi.keys
```