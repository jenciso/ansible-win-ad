## INSTALL

Ansible host:
```
sudo apt-get install -y libkrb5-dev
sudo pip install pywinrm[Kerberos]
sudo pip install --upgrade pip
``` 

Windows Server:
```
wget https://raw.githubusercontent.com/ansible/ansible/devel/examples/scripts/ConfigureRemotingForAnsible.ps1 -OutFile Ansible.ps1
./Ansible.ps1
``` 

Create OU:

CORP
  GROUPS
    DEPARTMENTS
    SERVICES
  USERS
    DEVS
    OPS
    HR


https://github.com/ianunruh/ansible-role-active-directory
https://6uellerbpanda.gitlab.io/posts/2018/04-17-Active-Directory-usermanagement-with-Ansible/
https://argonsys.com/microsoft-cloud/articles/configuring-ansible-manage-windows-servers-step-step/
https://www.youtube.com/watch?v=gJ81eaGlN_I
http://www.janua.fr/using-client-scope-with-redhat-sso-keycloak/
https://raw.githubusercontent.com/mrbobbytables/oidckube/master/k8s-realm-example.json
https://medium.com/@mrbobbytables/kubernetes-day-2-operations-authn-authz-with-oidc-and-a-little-help-from-keycloak-de4ea1bdbbe
https://medium.com/@int128/kubectl-with-openid-connect-43120b451672
https://itnext.io/protect-kubernetes-dashboard-with-openid-connect-104b9e75e39c
