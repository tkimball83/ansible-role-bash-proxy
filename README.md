# ansible-role-bash_proxy

[![Build Status](https://travis-ci.org/tkimball83/ansible-role-bash_proxy.svg?branch=master)](https://travis-ci.org/tkimball83/ansible-role-bash_proxy)
[![Ansible Galaxy](https://img.shields.io/badge/ansible--galaxy-bash_proxy-blue.svg?style=flat)](https://galaxy.ansible.com/tkimball83/bash_proxy)
[![License](https://img.shields.io/badge/license-GPLv3-brightgreen.svg?style=flat)](COPYING)

macOS - Configure proxies via command line

## Requirements

None

## Role Variables

Available variables are listed below, along with default values:

    bash_proxy_dest: "{{ ansible_env.HOME }}/.bash_proxies"
    bash_proxy_ftp: false
    bash_proxy_group: "{{ ansible_real_groupd_id }}"
    bash_proxy_http: false
    bash_proxy_https: false
    bash_proxy_mode: 0600
    bash_proxy_noproxy:
      - 127.0.0.1
      - localhost
    bash_proxy_owner: "{{ ansible_real_user_id }}"
    bash_proxy_rsync: false

Additional variables not defined by default:

    bash_proxy_ftp_host: localhost
    bash_proxy_ftp_pass: password
    bash_proxy_ftp_prot: http
    bash_proxy_ftp_port: 8080
    bash_proxy_ftp_user: username
    bash_proxy_http_host: localhost
    bash_proxy_http_pass: password
    bash_proxy_http_prot: http
    bash_proxy_http_port: 8080
    bash_proxy_http_user: username
    bash_proxy_https_host: localhost
    bash_proxy_https_pass: password
    bash_proxy_https_prot: https
    bash_proxy_https_port: 8080
    bash_proxy_https_user: username
    bash_proxy_rsync_host: localhost
    bash_proxy_rsync_pass: password
    bash_proxy_rsync_port: 1080
    bash_proxy_rsync_user: username

## Dependencies

None

## Example Playbook

    - hosts: servers
      roles:
        - role: tkimball83.bash_proxy
          bash_proxy_http: true
          bash_proxy_http_host: central.usa.torguardvpnaccess.com
          bash_proxy_http_pass: qRUPfS939oV4
          bash_proxy_http_prot: http
          bash_proxy_http_port: 6060
          bash_proxy_http_user: r6reicFhF7wG
          bash_proxy_https: true
          bash_proxy_https_host: central.usa.torguardvpnaccess.com
          bash_proxy_https_pass: qRUPfS939oV4
          bash_proxy_https_prot: http
          bash_proxy_https_port: 6060
          bash_proxy_https_user: r6reicFhF7wG

## License

Copyright (C) 2018 Taylor Kimball <tkimball@linuxhq.org>

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program. If not, see <http://www.gnu.org/licenses/>.
