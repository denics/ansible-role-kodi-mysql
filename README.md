kodi-mysql
===========

[![Galaxy](http://img.shields.io/badge/galaxy-GR360RY.kodi--mysql-green.svg?style=flat-square)](https://galaxy.ansible.com/list#/roles/3098)

An ansible role to setup and configure Kodi Mysql Database. This role creates empty Music and Videos Databases with preconfigured media paths.

Requirements
------------

This role requires Ansible 2.0 or higher. Platform requirements are listed in the metadata file.

Overview
--------

Role Variables
--------------

 name                       | default                              
----------------------------|----------
 kodi_mysqldb_user          | kodi
 kodi_mysqldb_password      | kodi


Dependencies
------------

Role Name| Description
----------|-----------
[![Galaxy](http://img.shields.io/badge/galaxy-GR360RY.htpc--common-blue.svg?style=flat-square)](https://galaxy.ansible.com/GR360RY/htpc-common/)| Create htpc user and media folders|

Variables defined in `GR360RY.htpc-common` role:

 Name                   | Default   
----------------------- |------------
 htpc_user_username     | htpc      
 htpc_user_password     | htpc      
 htpc_user_group        | htpc      
 htpc_user_shell        | /bin/bash 
 htpc_user_ssh_service  | yes       
 htpc_user_sudo_access  | yes       
 htpc_media_path        | /mnt/media
 htpc_media_movies      | movies    
 htpc_media_tv          | tv        
 htpc_media_music       | music     
 htpc_media_pictures    | pictures  
 htpc_media_downloads   | downloads
 htpc_zeroconf          | yes 


Example Playbook
-------------------------

Configure Kodi Mysql Database:

```
    - hosts: htpc

      vars:

        kodi_mysqldb_user: foo
        kodi_mysqldb_password: bar

      roles:
        - role: GR360RY.kodi-mysql
```

Configure Kodi together with Kodi Mysql Database ( download GR360RY.kodi-client role ):

```
    - hosts: htpc

      roles:
        - role: GR360RY.kodi-client
        - role: GR360RY.kodi-mysql
```


HTPC-Ansible Project
--------------------

This role is part of HTPC-Ansible project that includes additional roles for building Ubuntu Based HTPC Server.

 Role name               | Comment
-------------------------|-----------------------------
[![Galaxy](http://img.shields.io/badge/galaxy-GR360RY.htpc--common-blue.svg?style=flat-square)](https://galaxy.ansible.com/GR360RY/htpc-common)   | Create htpc user and media folders
[![Galaxy](http://img.shields.io/badge/galaxy-GR360RY.htpc--nas-blue.svg?style=flat-square)](https://galaxy.ansible.com/GR360RY/htpc-nas)         | Configure NAS ( NFS, CIFS and AFP )
[![Galaxy](http://img.shields.io/badge/galaxy-GR360RY.kodi--client-blue.svg?style=flat-square)](https://galaxy.ansible.com/GR360RY/kodi-client)   | Install Kodi Media Player
[![Galaxy](http://img.shields.io/badge/galaxy-GR360RY.kodi--mysql-blue.svg?style=flat-square)](https://galaxy.ansible.com/GR360RY/kodi-mysql)     | Install MySQL Backend for Kodi
[![Galaxy](http://img.shields.io/badge/galaxy-GR360RY.deluge-blue.svg?style=flat-square)](https://galaxy.ansible.com/GR360RY/deluge)              | Install Deluge Bittornet Client
[![Galaxy](http://img.shields.io/badge/galaxy-GR360RY.nzbtomedia-blue.svg?style=flat-square)](https://galaxy.ansible.com/GR360RY/nzbtomedia)      | Install NZBtoMedia Postprocessing
[![Galaxy](http://img.shields.io/badge/galaxy-GR360RY.sickrage-blue.svg?style=flat-square)](https://galaxy.ansible.com/GR360RY/sickrage)          | Install SickRage
<!-- 
[![Galaxy](http://img.shields.io/badge/galaxy-GR360RY.sabnzbd-blue.svg?style=flat-square)](https://galaxy.ansible.com/GR360RY/sabnzbd)            | Install Sabnzbd
[![Galaxy](http://img.shields.io/badge/galaxy-GR360RY.couchpotato-blue.svg?style=flat-square)](https://galaxy.ansible.com/GR360RY/couchpotato)    | Install CouchPotato
[![Galaxy](http://img.shields.io/badge/galaxy-GR360RY.htpc--manager-blue.svg?style=flat-square)](https://galaxy.ansible.com/GR360RY/htpc-manager) | Install htpc-manager
[![Galaxy](http://img.shields.io/badge/galaxy-GR360RY.tvheadend-blue.svg?style=flat-square)](https://galaxy.ansible.com/GR360RY/tvheadend)        | Install Tvheadend

Additional Info is available at [www.htpc-ansible.org](http://www.htpc-ansible.org)
 -->
License
-------

BSD

Author Information
------------------

Gregory Shulov