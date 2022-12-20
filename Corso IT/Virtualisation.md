
- **Hypervisor type 1** (Para virtualisation): the hypervisor creates the virtual machines and manages the resource access of the machines to the resources.
- **Hypervisor type 2**: the hypervisor creates instances of a virtual machine's OS but compete with other desktop apps (on the physical machine) for resources. Used for testing purpose.
- **Containers**: Each container share part of the kernel with the physical OS. The virtual machine can ONLY be ones that use the same kernel of the physical machine.

## Virtual NIC

- **Host**: Only the host PC is connected to internet
- **Bridge**: The PC and the Virtual machine are parallel linked to a switch
- **NAT**: The VM is connected to internet through the host PC. The host translates the source IP from the VM in its IP.
