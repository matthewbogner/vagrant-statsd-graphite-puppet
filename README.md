# statsd + graphite Vagrant #

Provision a virtual machine with vagrant and puppet including statsd and graphite.

## Prerequisites ##
 * Install VirtualBox https://www.virtualbox.org/wiki/Downloads
 * Install Vagrant http://docs.vagrantup.com/v2/installation/index.html
 * git clone https://github.com/matthewbogner/vagrant-statsd-graphite-puppet

## Usage ##

`vagrant up`
`vagrant provision` 

## Ports ##

  * **Graphite Web**: http://localhost:8034/
  * **statsd**: 8125:udp
  
  
  
