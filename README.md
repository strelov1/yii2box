## Yii2 Advanced Project + Vagrant VM + Ansible provisioning

## Out of the box...

* Ubuntu 14.04 64 bit
* PHP-FPM 5.6 ( + modules `intl`, `gd`, `xdebug` etc.)
* Nginx 1.8
* MySQL 5.5
* Composer
* Memcached 1.4.14 ( + php5_memcached)
* Yii2 Advanced Project

### Install

* [Virtualbox 4.3+](https://www.virtualbox.org/) + VirtualBox Extension Pack
* [Vagrant 1.7+](http://www.vagrantup.com/)
additional Vagrant modules will be installed automatically (vagrant-hostmanager, vagrant-vbguest, vagrant-cachier)`

### RUN

* Clone this sources from Git
* Insert github_oauth_token in vars.yml
* Run `vagrant up`.

Ok, now if everything went fine you can access these Urls in your browser

* [http://yii2box/](http://yii2box/)  -  frontend app
* [http://backend.yii2box/](http://backend.yii2box/)  -  backend app


### Made by [Strelov Ilya]