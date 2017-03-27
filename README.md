# ansible-role-bash-proxy

[![Build Status](https://travis-ci.org/tkimball83/ansible-role-bash-proxy.svg?branch=master)](https://travis-ci.org/tkimball83/ansible-role-bash-proxy)

macOS - Configure proxies via command line

## Requirements

None

## Role Variables

Available variables are listed below, along with default values:

    bash_proxy_ftp: False
    bash_proxy_http: False
    bash_proxy_https: False
    bash_proxy_rsync: False
    bash_proxy_noproxy:
      - 127.0.0.1
      - localhost

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
    bash_proxy_https_port: 8443
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
        - role: tkimball83.bash-proxy
          bash_proxy_http: True
          bash_proxy_http_host: central.usa.torguardvpnaccess.com
          bash_proxy_http_pass: qRUPfS939oV4
          bash_proxy_http_prot: http
          bash_proxy_http_port: 6060
          bash_proxy_http_user: r6reicFhF7wG
          bash_proxy_https: True
          bash_proxy_https_host: central.usa.torguardvpnaccess.com
          bash_proxy_https_pass: qRUPfS939oV4
          bash_proxy_https_prot: http
          bash_proxy_https_port: 6060
          bash_proxy_https_user: r6reicFhF7wG

## License

BSD

## Author Information

This role was created by [Taylor Kimball](http://www.linuxhq.org).
