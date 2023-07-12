# [←](..) 📖 `all-gatherfacts` playbook

Gather facts and packages facts for all system in the inventory. Write those facts in a local file in the folder [`facts`](../facts/).


## Usage

```console
ansible-playbook all-gatherfacts.yml
```


## Tags

- `all` to run the whole playbook.
- `clean` to delete the facts folder.
- `facts` to run only the gather facts.
- `pkgs` to run only the packages facts.


