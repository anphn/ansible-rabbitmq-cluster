# Rabbitmq-cluster-ansible

## Requirements

* Ansible
* RHEL/CentOS 7
* Ubuntu 16.04
* Disable Selinux

## Role Variables

Available variables are listed below, along with default values (see defaults/main.yml):

``` bash

## chooses your clustername
rabbitmq_cluster_name

## config user password for rabbitmq

rabbitmq_auth_user: rabbit
rabbitmq_auth_password: Jd0Hs5XHmFrJzPTW

## erlang cookie
rabbitmq_cookie_token: Jd0Hs5XHmFrJzPTW

## enable plugin dashboard
rabbitmq_plugins:
  - name: rabbitmq_management
    state: enabled

```
## inventory

* See inventory.ini. 
* Change your server ip in inventory.ini in groups rabbitmq

### Run

    $ git clone https://github.com/anphn/ansible-rabbitmq-cluster.git
    $ cd ansible-rabbitmq-cluster
    $ ansible-playbook -i inventory.ini setup-message-queue.yml
