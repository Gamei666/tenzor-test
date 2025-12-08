Vbox+TestVM        
=========

Роль устанавливает VirtualBox в ОС семейства RHEL или Debian используя пакетные менеджеры dnf и apt соответственно. Затем устанавливает последнюю версию Vagrant из зеркала в YandexCloud.

Requirements
------------

ОС семейства RHEL или Debian с соответствующими пакетными менеджерами.

Role Variables
--------------

vm_dir: Папка установки ВМ

Переменные для Vagrant
vagrant:
    vg_name: Имя ВМ Vagrant
    box_url: https://cloud.centos.org/centos/9-stream/x86_64/images/CentOS-Stream-Vagrant-9-latest.x86_64.vagrant-virtualbox.box
    net_name: Имя хоста
    disksize: Размер диска (в GB)
    cpu: кол-во CPU
    vb_name: Имя в VirtualBox
    memory: Выделяемая память
    ip: IP-адрес, учитывайте, что стандартная подсеть в VirtualBox 192.168.56.0/24 соответственно попытка выдать адрес вне этой сети приведёт к ошибке.

Dependencies
------------

-

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - vboxhost

License
-------

BSD

Author Information
------------------

