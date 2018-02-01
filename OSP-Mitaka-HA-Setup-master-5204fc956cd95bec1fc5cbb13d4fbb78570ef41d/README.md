# openstack-mitaka-ha-ansible
Openstack mitaka setup with HA
=======

Harware and Software requirements:
----------------------------------
1) If you are installing Openstack HA setup on Bare metal Hardware, install Ubuntu 14.04 on all the nodes and two NIC cards (one with Private IP address and anther for Public).

2) For testcase, we have used VirtualBox with Ubuntu 14.04 installed on all the nodes and 2 adaptars (if you not using NAT for the hostonly adapters, add one more adaptar for each VMs for installing packages).

3) Below figure will illustrate the articeture of the Openstack HA Miataka:


Overview of the Mitaka HA setup:
---------------------------------
1) This openstack Mitaka setup HA uses three controller nodes (Both controller and network on single controller node) and one compute node

2) For MySQL database replication, we have used Percona XtraDB Cluster.

3) RabbitMQ cluster is used for maintaining the message queue on failover.

4) On controller nodes, we are using pacemaker cluster with corosync for API service replication.
