# telerec-t-semaphore
Semaphore submodule for Telerect

Add this role with:
```shell
git submodule add git@github.com:pinae/telerec-t-semaphore.git roles/semaphore
```

## Configuration
Please change the passwords! A block like this lives in `group_vars/all.yml`:
```yaml
semaphore:
  name: semaphore
  directory: "{{ docker_dir }}/semaphore"
  domain: "semaphore.example.com"
  #url_path_prefix: "/semaphore"  ## Use this if you have a home server without subdomains 
  postgres_password: "change_me_to_something_secret"  # Generate your own with: tr -dc A-Za-z0-9_ < /dev/urandom | head -c 26 | xargs
  admin_password: "password_to_change"  # Generate your own with: tr -dc A-Za-z0-9_ < /dev/urandom | head -c 18 | xargs 
  access_key_encryption: "l+ORkbPYbizk2doreMI1VlNpHcJ8AUUlNfvgfjVA2Aw="  # Generate your own with: head -c32 /dev/urandom | base64
```