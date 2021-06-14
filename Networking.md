# Raspberry Pi #

## Connect the Raspberry pi to virtual machine ##

![Overview vm connection](VmConnection)

Additional: Have internet on the VM as well

- Host System: Enable dynamic ip ranging on the Ethernet device

- VM Settings: Set up two network connection
  - NAT
  - Bridge, connected to the physical Ethernet connection with dynamic range

- Set a static ip inside VM environment
- Use nmap to find the raspberry pi -> `nmap -n -p 22 --open <StaticIp>`

- connect
