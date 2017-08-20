

Host OS:
	CentOS 7.x
	*yum groupinstall "GNOME Desktop"
	CPU/MMU Virtualization enabled (Intel VT-x/AMD-V)



System Requirements - packages and their dependencies:
	Git
		yum install git
	Desktop Virtualization using VirtualBox on CentOS 7.3
		cd /etc/yum.repos.d/
		wget http://download.virtualbox.org/virtualbox/rpm/rhel/virtualbox.repo
		yum -y install VirtualBox-5.1
		Rebuild kernel modules with following command:
		yum install gcc make
		rpm -Uvh https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm
		yum install binutils gcc make patch libgomp glibc-headers glibc-devel kernel-headers kernel-devel dkms
		wget ftp://ftp.pbone.net/mirror/ftp.scientificlinux.org/linux/scientific/7.0/x86_64/updates/security/kernel-devel-3.10.0-327.el7.x86_64.rpm
		yum install ./kernel-devel-3.10.0-327.el7.x86_64.rpm
		Now we are ready to Build VirtualBox kernel modules
		/usr/lib/virtualbox/vboxdrv.sh setup
		To install VirtualBox Extension Pack:
		- Find virtualbox release - ours is 5.1.26 - Browse below link: 
		download.virtualbox.org/virtualbox/5.1.26
	
		Add VirtualBox User(s) to vboxusers Group
		usermod -a -G vboxusers localuser


	
	Ansible
	Vagrant
		wget https://releases.hashicorp.com/vagrant/1.9.7/vagrant_1.9.7_x86_64.rpm
		yum install ./vagrant_1.9.7_x86_64.rpm

		vagrant init precise64 http://files.vagrantup.com/precise64
		vagrant up

		" Getting Vagrant file from Fedora Project: https://fedoraproject.org/wiki/Vagrant "
		




	Python

	Ruby
		sudo apt-get -y  install ruby
		sudo apt-get install bundler
		cd /vagrant/simple-sinatra-app 
		bundle install/vagrant/simple-sinatra-app

		bundle install
		bundle exec rackup
		sudo bundle exec rackup -p 80
		sudo bundle exec rackup -p 80 -o 10.0.2.15



- log in as normal user
- mkdir REA	# create project directory
- retrieve Vagrantfile from Github
- vagrant up
- 



