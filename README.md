# ams-roles
# First create a folder named ams-roles for roles using
ansible-galaxy init ams-roles

# Put your playbooks inside this ams-roles folder

# Copy your sql dump into /tmp directory
flasktab.sql

# Then create and execute your main file "ams.yml" for making app live by firing
ansible-playbook ams.yml

