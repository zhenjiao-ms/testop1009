You open a port, or create an endpoint, to a virtual machine (VM) in Azure by creating a network filter on a subnet or VM network interface. You place these filters, which control both inbound and outbound traffic, on a Network Security Group attached to the resource that receives the traffic.

Let's use a common example of web traffic on port 80. Once you have a VM that is configured to serve web requests on the standard TCP port 80 (remember to start the appropriate services and open any OS firewall rules on the VM as well), you:

1. Create a Network Security Group.
2. Create an inbound rule allowing traffic with:
   * the destination port range of "80"
   * the source port range of "*" (allowing any source port)
   * a priority value of less 65,500 (to be higher in priority than the default catch-all deny inbound rule)
3. Associate the Network Security Group with the VM network interface or subnet.

You can create complex network configurations to secure your environment using Network Security Groups and rules. Our example uses only one or two rules that allow HTTP traffic or remote management. For more information, see the following ['More Information'](#more-information-on-network-security-groups) section or [What is a Network Security Group?](../articles/virtual-network/virtual-networks-nsg.md)

