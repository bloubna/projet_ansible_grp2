#  Démarrage environnement Ansible et projet Git Ansible

GRP2 :
poecdevops.grp2.dawan.training
user : stagiaire
mdp : P0ec2021!
sudo avec mot de passe

ssh-copy-id stagiaire@poecdevops.grp2.dawan.training

ansible debianserver -i inventory -m ping

##Creation du playbook pour initier la création du user ansible dans le server à distance

ansible-playbook  -b -e cible=serversible --user stagiaire  bootstrap_playbook.yml