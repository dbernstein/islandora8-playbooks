# islandora8-playbooks

### Prerequisites
* ansible 2.7.10
* ec2.py and ec2.ini

```
curl https://raw.githubusercontent.com/ansible/ansible/devel/contrib/inventory/ec2.py > ec2.py
curl https://raw.githubusercontent.com/ansible/ansible/devel/contrib/inventory/ec2.ini > ec2.ini
```

### Run
```
AWS_PROFILE=<your aws profile>  ansible-playbook -i ec2.py  --private-key <path/to/your/private/key.pem>  --user ubuntu --limit 'tag_Islandora8_true:&tag_Shared_true'  shared-resources-playbook.yml
```
