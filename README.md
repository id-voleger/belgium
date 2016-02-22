# Drupal 6 site VM

### Steps to start
* Install the latest versions of Vagrant, VirtualBox and Ansible.
* Fork this repository or just copy its files.
* Get latest Ansible roles form the cloud with command:
  **sudo ansible-galaxy install -r requirements.txt --force**
* Create **db/** and **site/** folders.
* Copy site's files into **site/** folder and database dump into **db/** folder.
* Open **config.yml**.
* Change **SITE_NAME** to the domain name of your site.
* Change **DUMP_FILE** to the filename of your dump.
* Add **192.168.33.20 <your_site_domain.be>** to your host's machine
  **/etc/hosts** file.
* Execute **vagrant up**.

If you want to redeploy your site then run **vagrant provision**.
Server packages won't be reinstalled if configs were not changed.
