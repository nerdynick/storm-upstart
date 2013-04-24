=============
storm-upstart
=============

This is just a small collection of upstart config scripts to startup a storm cluster and its components. 

Install
-------

By default these upstart configs assume you will be running your process as the user storm and the group storm. As well as storm is installed in /opt/storm.
You do not have to stick to this setup. You just simple need to change the INSTALL_DIR value and setuid/setgid blocks to your respected values.

Installation is as simple as coping the respected config to /etc/init on the hosts you wish to run that given service.

- storm-nimbus.conf - Nimbus Node
- storm-super - Supervisor Node
- storm-ui - Web UI Node. Easiest is to just place this on the same node as you wish to run your nimbus deamon

Starting/Stopping
-----------------

start
    sudo start storm-nimbus
    sudo start storm-ui
    sudo start storm-super

stop
    sudo stop storm-nimbus
    sudo stop storm-ui
    sudo stop storm-super

