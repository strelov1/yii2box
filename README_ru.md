## Yii2 Advanced Project + Vagrant VM + Ansible provisioning

## Что входит в этот box...

* Ubuntu 14.04 64 bit
* PHP-FPM 5.6 ( + modules `intl`, `gd`, `xdebug` и т.д.)
* Nginx 1.8
* MySQL 5.5
* Composer
* Memcached 1.4.14 ( + php5_memcached)
* Yii2 Advanced Project

### Установка

* [Virtualbox 4.3+](https://www.virtualbox.org/) + VirtualBox Extension Pack
* [Vagrant 1.7+](http://www.vagrantup.com/)
дополнительные Vagrant модули установятся автоматически (vagrant-hostmanager, vagrant-vbguest, vagrant-cachier)`

### Запуск

* Клонируйте этот репозиторий
* Вставтье свой github_oauth_token в vars.yml
* Запустите командой `vagrant up`.

Если все прошло успешно вы можете открыть в браузере

* [http://yii2box/](http://yii2box/)  -  frontend app
* [http://backend.yii2box/](http://backend.yii2box/)  -  backend app


### Made by [Strelov Ilya]