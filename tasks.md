# these are the things I want to accomplish
## hosts file with ip of vm
     
## generate an ssh key and add to authorized_keys for the virtual machine

   ssh-keygen -t rsa -C "your_email@example.com" -f ./deploy
   

   .env/bin/ansible 192.168.1.12 -m file -a "state=directory mode=0700 dest=/root/.ssh/" -u vagrant -i hosts -k -c paramiko -s
   .env/bin/ansible 192.168.1.12 -m copy -a "src=deploy.pub dest=/root/.ssh/authorized_keys owner=root mode=0600" -u vagrant -i hosts -k -c paramiko -s

## learn ansible

http://www.ansibleworks.com/quickstart-video/



you can pass a python module on the cmd line.
https://raw.github.com/ansible/ansible/devel/plugins/inventory/ec2.py
http://www.ansibleworks.com/docs/intro_dynamic_inventory.html#example-aws-ec2-external-inventory-script


here's some examples.
https://github.com/ansible/ansible-examples


## bring up a ruby app server



## bring up a postgres db server

## bring up a solr instance
   - config
   - schema
   
## deploy viper app
   - create db
   - create users
   - migrate schema

## bring up unicorn
## bring up nginx
## bonus: nagios
