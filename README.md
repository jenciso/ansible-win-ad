## Windows AD playbook


### Pre-configuração

Para usar este playbook precisa configurar no lado do servidor windows
```
wget https://raw.githubusercontent.com/ansible/ansible/devel/examples/scripts/ConfigureRemotingForAnsible.ps1 -OutFile Ansible.ps1
./Ansible.ps1
```

E no lado do ansible:
```
sudo apt-get install -y libkrb5-dev
sudo pip install pywinrm[Kerberos]
sudo pip install --upgrade pip
```

### Active Direcory OU


```
CORP.ENCISO.WEBSITE
   CORE
      GROUPS
          DEPARTMENTS
            * DEVS
            * OPS
            * ADM
          SERVICES
            * sudoers
            * gitlab
	    * nx-adm
      USERS
          DEPARTMENTS
              DEVS
                * Developer01
                * Developer02
              OPS
                * Operator01
	        * Operator02
              ADM
                * Administrator01
          SERVICES
                * ansible
```

###  Users and Groups

Ficam nas variaveis:
```
group_vars/all/users.yml
group_vars/all/groups.yml
```

### Configuração

* Criar o arvore OU como está na figura

![AD_OU](https://i.imgur.com/49zMnTQ.png)

* Rodar o playbook para criar os usuarios e grupos

```
ansible-playbook -i inventory site.yml
``` 
