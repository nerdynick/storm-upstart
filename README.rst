=============
storm-upstart
=============

This is just a small collection of `upstart <http://upstart.ubuntu.com/>`_ config scripts to startup a storm cluster and its components. 

=================  ============  ===============
Config File        Service Name  Description
=================  ============  ===============
storm-nimbus.conf  storm-nimbus  Nimbus Node
storm-super.conf   storm-super   Supervisor Node
storm-ui.conf      storm-ui      Web UI Node
=================  ============  ===============

Install
-------

By default these upstart configs assume you will be running your process as the user storm and the group storm. As well as storm is installed in /opt/storm.
You do not have to stick to this setup. You just simple need to change the INSTALL_DIR value and setuid/setgid blocks to your respected values.

Installation is as simple as coping the respected config to /etc/init on the hosts you wish to run that given service.

Starting/Stopping
-----------------

start
    sudo start <SERVICE_NAME>

stop
    sudo stop <SERVICE_NAME>
