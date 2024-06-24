# Cowrie_Ansible
playbook Ansible pour installer et configurer Cowrie, un honeypot SSH interactif. Ce playbook configure également les redirections de ports nécessaires et met en place les permissions pour Authbind.

# Architecture
```plaintext
cowrie_ansible/
│
├── cowrie_install.yaml   
├── hosts.ini             
└── README.md
```

# Utilisation
Clonage du dépot Github:
```
git clone https://github.com/Jbrt35/Cowrie_Ansible.git
cd Cowrie_Ansible
```

```
ansible-playbook -i hosts.ini cowrie_install.yaml
```
Ce playbook démarrer automatiquement le honeypot Cowrie pour le couper
```
bin/cowrie stop
```

# Problème potentiel

L'utilisateur avec lequel doit s'éxécuter le playbook Ansible ne doit pas être administrateur car sinon cela empêche cowrie de démarrer
