Welcome to the EGW wiki! EGW(external gateway) run on dpdk. EGW is used for Layer-4/7 load balancer and NATGW and VPC cloud network.

## Use Case：

![](https://github.com/SDN-NFV-DEV/EGW/blob/master/picture/egw-scene.png)

## Network Topology：
![](https://github.com/SDN-NFV-DEV/EGW/blob/master/picture/egw-deploy.png)

## Software Architecture:

![](https://github.com/SDN-NFV-DEV/EGW/blob/master/picture/egw-architecture.png)

### Major features

* L4 Load Balancer: work for tunnel mode.
* L7 Load Balancer: Support http. FLow of https will be change to L4 LB.
* NAT gate way: Support dynamic nat and conntrack. Suitable for use as security gateway.
* VPC module: include vpc-lb and vpc-nat fuction. Support standard vxlan protocol.
* Security: Support TCP syn-proxy,UDP Anti Attack,Conntrack,url check.
* QoS: Traffic Control.
* Cluster: Support cluster sync by multicast and unicast. Integrated OSPF and BGP.
* Prober: Support fault detection like BFD.
* User-space IP stack (ARP, ICMP LLDP ...).

## Quick Start

### Environment
* Linux Distribution: CentOS 7.3
* Kernel: 3.10.0-514.el7.x86_64
* gcc version 4.8.5 20150623 (Red Hat 4.8.5-11) (GCC) 
* CPU: Intel E5-2626 (User custom)
* NIC: E1000,Intel 82599,XL710.(User custom)
* Memory: 64G with two NUMA node.(User custom)

### License
The purpose of licenseis to count the number of user. Please send "server Serial Number" to the the email(1534898891@qq.com). I will return the licenseis to you as soon as possible.

### Install EGW

`git clone https://github.com/SDN-NFV-DEV/EGW.git`        
`cd EGW/release/`         
`tar -mzxf EGW_V1.0.tar.gz`     
`./install_egw.bin all`     

### Config EGW

`cd /usr/local/egw/sbin/`        
`vi egw_service.sh`

### Launch EGW
`cd /usr/local/egw/sbin/`     
`./egw.sh`

### EGW LOG
egw log is at /data/egw/log/egw.log

## Contact Us
email: 1534898891@qq.com              
qq group: 809768874
