# TP_Ansible
Cours Ansible

# TP 1 : Installation apache:
```bash
ansible-playbook apache.yml -i inventory.ini --become --ask-become-pass
```

# TP 2: Installation gitlab:

## Pour ubuntu 20.04:
Basculer sur le repo de ubuntu 18.04 (bionic)
```bash
sudo tee /etc/apt/sources.list.d/gitlab_gitlab-ce.list<<EOF
deb https://packages.gitlab.com/gitlab/gitlab-ce/ubuntu/ bionic main
deb-src https://packages.gitlab.com/gitlab/gitlab-ce/ubuntu/ bionic main
EOF
```

Désactiver l'execution du .sh dans le fichier yaml

puis executer:
```bash
ansible-playbook main.yml -i inventory.ini --become --ask-become-pass
```
