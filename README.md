Create a local self contained environment for app developerment/deployment.

Includes Java, Maven, rvm, mongodb

##Installation reqs

* VirtualBox (tested w/ 5.0.16)
* Vagrant (tested w/ 1.8.1)
* Ruby (tested w/ 2.0.0)
* ChefDK (tested w/ 0.12.0)
  
##Install the following if not already on your local machine:
  1. Download and install VirtualBox: https://www.virtualbox.org/
  2. Download and install Ruby (tested with 2.0.0)
  3. Download and install Vagrant: https://www.vagrantup.com/
  4. Download and install Chef: https://downloads.chef.io/chef-dk
  5. Install the Vagrant Berkshelf plugin:
   ```
   vagrant plugin install vagrant-berkshelf
   ```
  6. Install the Vagrant omnibus plugin: 
   ```
   vagrant plugin install vagrant-omnibus
   ```   
  7. Generate 'Vagrantfile' by executing the following by providing the path to your project directory:
  ```
  ruby config_vagrant.rb -l /path-to-your-project-to-be-mounted-on-vagrant-box
  ```

  ** Your project directory will be mounted at /vagrant_data 
  8. Create a folder "cookbooks" where Berkself can download the cookbooks
  9. (Optional - if downloading box takes too long in #9) Download and install ubuntu/trusty64 box: 
  	 1. Download box from http://cloud-images.ubuntu.com/vagrant/trusty/current/trusty-server-cloudimg-amd64-vagrant-disk1.box
  	 2. Add the box to vagrant
  	 ```
  	 vagrant box add ubuntu/trusty64 /path-to-downloaded-box/trusty-server-cloudimg-amd64-vagrant-disk1.box
  	 ```

  10. From terminal enter the command "vagrant up" to create the vagrant box and run the install script
  
  11. After the vagrant box is created, enter 'vagrant ssh' to access the vagrant box from the terminal
  
  12. Your Vagrant box will be available at 192.168.33.10 on your host machine


