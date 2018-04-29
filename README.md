kodi-mysql
===========

[![Galaxy](http://img.shields.io/badge/galaxy-GR360RY.kodi--mysql-green.svg?style=flat-square)](https://galaxy.ansible.com/GR360RY/kodi-mysql)

An ansible role to setup and configure Kodi Mysql Database. This role creates empty Music and Videos Databases with preconfigured media paths.

Requirements
------------

This role requires Ansible 2.0 or higher. Platform requirements are listed in the metadata file.

Overview
--------

List of tasks that will be performed under kodi-mysql role:

* Install Kodi
* Install MySQL Server
* Configure MySQL Server to Listen on All Interfaces
* Create MySQL User for Kodi Music and Videos Databases with preconfigured media paths
* If Music and Videos Databases are already in place, skip database import