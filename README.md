vagrant-elasticsearch-ansible
=============================

DevOps demonstration for provisioning a Vagrant VM with Elasticsearch and Kibana.
You will be able to start indexing data on Elasticsearch with minimal setup time.

Please message me if you have any feedback or questions!

Required software
=============================

Vagrant: http://downloads.vagrantup.com/

Oracle JDK: https://www.google.com/search?q=oracle+jdk

  You could use openjdk, but from the elasticsearch workshop I attended, the core dev's recommended Oracle.
  I won't be able to include this in the git repo due to the Oracle license but I'll make a marker for it.
  
Ansible: https://github.com/ansible/ansible

Setup on MacOSX (works for me.)
======

easy_install virtualenv

virtualenv ansible-env

source ansible-env/bin/activate

Next two lines might be optional (was required for me in 10.6.8, but not anymore in mavericks)

  sudo bash
  export ARCHFLAGS='-arch i386 -arch x86_64'

sudo easy_install pip

sudo pip install paramiko PyYAML jinja2

Reference from https://weluse.de/blog/installing-ansible-on-os-x.html

After setup...

Run ./provisioning/provision-vm-development and let it run!

=========
Deploying to EC2

You don't have to configure the Vagrantfile, all you need to do is modify the host file and copy the jdk file to 
the VM. 
