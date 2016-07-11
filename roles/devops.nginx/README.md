# Ansible Role: nginx

Installs and Configures Nginx.

## Requirements

None.

## Role Variables

### `defaults/main.yml`

* nginx_repo_enable: true
* nginx_repo_baseurl: http://nginx.org/packages/centos/{{ ansible_distribution_major_version }}/$basearch/
* `nginx_remove_default_vhost: false`
* `nginx_worker_processes: "auto"`
* `nginx_events_worker_connections: "1024"`
* `nginx_events_use: ""`
* `nginx_error_log: "/var/log/nginx/error.log warn"`
* `nginx_access_log: "/var/log/nginx/access.log main"`
* `nginx_sendfile: "on"`
* `nginx_tcp_nopush: "on"`
* `nginx_tcp_nodelay: "on"`
* `nginx_keepalive_timeout: "65"`
* `nginx_types_hash_max_size: "2048"`
* `nginx_client_max_body_size: ""`
* `nginx_proxy_cache_path: ""`
* `nginx_conf_extra_parameters: []`
* `nginx_vhosts: []`
* `nginx_vhosts_files: []`

### `vars/RedHat.yml`
vars for RedHat/CentOS

* `nginx_conf_path: /etc/nginx/conf.d`
* `nginx_vhost_path: /etc/nginx/conf.d`
* `nginx_default_vhost_path: /etc/nginx/conf.d/default.conf`
* `nginx_user: nginx`

## Dependencies

None.

## Example Playbook

    - hosts: servers
      roles:
         - role: nginx
           nginx_conf_extra_parameters:
             - server_names_hash_bucket_size 64

## Author Information

z
