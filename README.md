1. Установил VirtrualBox.
2. Установил Vagrant.
1. Создать виртуальную машину из образа `debian/contrib-jessie64` и настроить не получилось. Собрал ВМ на образе Ubuntu `bento/ubuntu-18.04`.
1. Vagrant provisioner (Ansible) установлены требуемые пакеты, кроме PHP5.6 (не смог найти откуда его скачать). `Nginx` работает на `80` порту, `Apache2` на `8888` порту.  
    * Работа Playbook.  
        ![result](https://github.com/Rain-m-a-n/officemag/blob/master/pics/apache.png)
    * Работа Nginx.  
        ![result](https://github.com/Rain-m-a-n/officemag/blob/master/pics/nginx.png)
    * Работа Apache2.  
        ![result](https://github.com/Rain-m-a-n/officemag/blob/master/pics/apache.png)
1. Через плейбук заменил стартовую страницу web сервера. 
1. Заменить версию PHP (пример `replace.yml`) - не работает.
