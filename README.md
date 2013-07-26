# Base Configuration #

- Install Vagrant and VirtualBox
- Change the following files to fit your needs:

- Lines 6, 7, 8 - ./Vagrantfile

- Update the domain name you want to access the site under on line 3, and the public path 5 & 11. - ./puppet/modules/apache_vhosts/files/000_site

- If you don't need some of the modules, just remove them from line 18. - ./puppet/manifests/site.pp

