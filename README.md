# Creating Ams roles
  This repo contains role for installing and make AMS app live

- First create a folder named "ams-roles" for roles using below command
  ansible-galaxy init ams-roles

- Then inside "ams-roles" you can check many folders have been created and inside these
  eg: tasks,handlers etc.. we create yml playbooks to get the specific output.
  
- In cd ams-roles/tasks  you can see many .yml files and these all .yml files have different purpose such as

1) "install_redis.yml" used to install and start the redis.
2) "install_python3_pip3.yml" used to install pip3 and python3.
3) "install_python_utilities.yml" used to install python dependencies eg: flask etc..
4) "install_wkhtml.yml" used to install wkhtml utility.
5) "install git.yml" used to install git.
6) "clone_repo.yml" is used to create a directory and clone a git repository.
7) "install_and_start_mysql.yml" used to install and start mysql for your application.
8) "create_mysqluser_copy_credentials.yml" used to create a mysql user and copy user credentials.
9) "create_db_and_export_dump.yml " used to create a database and to import the databse.
10) Last is "main.yml"-> we have defined all the the above .yml files and a small script in "main.yml" because when we fire our playbook "ams.yml" which is kept outside "ams-roles" folder , it will first look for main.yml file inside the tasks folder.
# Copy your sql dump into /tmp directory
flasktab.sql

# Then create and execute your main file "ams.yml" for making app live by firing
ansible-playbook ams.yml

