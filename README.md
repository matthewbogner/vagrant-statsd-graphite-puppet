# statsd + graphite Vagrant #

Provision a virtual machine with vagrant and puppet including statsd and graphite.

 * debian package for statsd (github.com/etsy) included 

## Base Box ##

This setup expects a box with name `ubuntu12` based on http://files.vagrantup.com/precise64.box

## Usage ##

`vagrant up`


## Ports ##

  * **Graphite Web**: http://localhost:8034/
  * **statsd**: 8125:udp
  
  
  
