Experiments with [Ansible](http://ansible.cc)

All of these have only been tested on Ubuntu 12.04.

## Vagrant Integration

If you have [vagrant-ansible](https://github.com/dsander/vagrant-ansible) installed, you can test these by

```
$ vagrant up
# tweak ansible playbooks
$ vagrant provision
```

For now to test different playbooks the ``Vagrantfile`` must be tweaked.

## Ansible Playbooks

#### newservers

Some basic configs to apply to new servers.

Almost a complete ripoff of [5 minute bootstrap](https://github.com/phred/5minbootstrap).

* Upgrade all packages
* Automatically get Security Updates
* Run Fail2Ban
* Run LogWatch

```
$ ansible-playbook --sudo newservers/newservers.yml
```



#### Bitlbee

Provides a secured, password protected Bitlbee server. 

Generally a port of [MJ's Salt States](https://github.com/therevmj/salt-states)

* Runs stunnel with a self-signed cert on port 6697
* Allows you to enter login and oper passwords from the command line

```
$ ansible-playbook --sudo bitlbee/main.yml
```
