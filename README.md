# Ansible Role: ansible-apps_nfs

## Description

[![Build Status](https://travis-ci.com/lotusnoir/ansible-apps_nfs.svg?branch=master)](https://travis-ci.com/lotusnoir/ansible-apps_nfs)[![License](https://img.shields.io/badge/license-MIT%20License-brightgreen.svg)](https://opensource.org/licenses/MIT)[![Ansible Role](https://img.shields.io/badge/ansible%20role-apps__nfs-blue)](https://galaxy.ansible.com/lotusnoir/ansible-apps_nfs/)[![GitHub tag](https://img.shields.io/badge/version-latest-blue)](https://github.com/lotusnoir/ansible-apps_nfs/tags)

Deploy nfs mount point using ansible.


## Role variables

| Name           | Default Value | Description                        |
| -------------- | ------------- | -----------------------------------|
| `nfs_version` | 0.8.0 | nfs version |
| `nfs_binary_file` | /usr/local/bin/nfs | nfs binary name|

## Examples

	---
	- hosts: apps_nfs
	  become: yes
	  become_method: sudo
	  gather_facts: yes
	  roles:
	    - role: ansible-apps_nfs
	  environment: 
	    http_proxy: "{{ http_proxy }}"
	    https_proxy: "{{ https_proxy }}"
	    no_proxy: "{{ no_proxy }}

## License

This project is licensed under MIT License. See [LICENSE](/LICENSE) for more details.
