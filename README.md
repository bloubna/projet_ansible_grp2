#  Démarrage environnement Ansible et projet Git Ansible

GRP2 :
poecdevops.grp2.dawan.training
user : stagiaire
sudo avec mot de passe

ssh-copy-id stagiaire@64.227.125.8

ansible debianserver -i inventory -m ping

# Creation du playbook pour initier la création du user ansible dans le server à distance

ansible-playbook bootstrap_playbook.yml --user stagiaire -b --ask-become-pass

# Lancement du playbook requirement pour l'installation du role ansible-role-docker__3.1.2
ansible-galaxy role install -f roles/requirements.yml -p roles

# Lancement du playbook deploy-docker
ansible-playbook deploy-docker.yml