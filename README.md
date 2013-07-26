# Base Configuration #

- Install Vagrant and VirtualBox
- Change the following files to fit your needs:
-- ./Vagrantfile - Lines 6, 7, 8
-- Update the domain name you want to access the site under on line 3: ./puppet/modules/apache_vhosts/files/000_site
-- If you don't need some of the modules, just remove them from line 18 of: ./puppet/manifests/site.pp

