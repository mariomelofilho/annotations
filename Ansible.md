# Ansible Vault

## Encrypting a Variable in a yml.


 Original Yml:

```bash
cat segredo.yml
```

```yaml
---
service_user: srcuser
service_password: cleartextpassword

```

1. We'll encrypt only service_password variable
  1. Create a key_file that contains a key that will encrypt service_password variable value. Keep this file very safe and  never commit it in git

  ```bash
    cat key_file
  ```

  ```
  supersecrectkey
  ```

  2. We'll use a vault-id: my_vault_id. It is used to identify uniquely the encryption payload in ansible (including ansible-playbook and awx/tower)

  2. to encrypt  the content of service_password variable insice segredo.yml, using a vault-id called my_vault_id wit a key supersecretkey located inside key_file file, run the command:

```
ansible-vault encrypt_string --encrypt-vault-id 'my_vault_id' --vault-id my_vault_id@key_file  --name 'service_password' 'cleartextpassword'
```
